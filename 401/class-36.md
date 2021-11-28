# Amazon Cognito

Amazon Cognito User Pools is a full-featured user directory service to handle user registration, storage, authentication, and account recovery. Cognito User Pools returns JWT tokens to your app and does not provide temporary AWS credentials for calling authorized AWS Services. Amazon Cognito Federated Identities on the other hand, is a way to authorize your users to use AWS services. With an identity pool, you can obtain temporary AWS credentials with permissions you define to access other AWS services directly or to access resources through Amazon API Gateway.

## Configure Auth Category
- start amplify add auth
- push amplify push
- add dependency implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
- Add the Auth plugin before calling Amplify.configure


## Register a user
call

     AuthSignUpOptions options = AuthSignUpOptions.builder()
    .userAttribute(AuthUserAttributeKey.email(), "my@email.com")
    .build();
      Amplify.Auth.signUp("username", "Password123", options,
    result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
    error -> Log.e("AuthQuickStart", "Sign up failed", error)
      );

- Enter the confirmation code received via email in the confirmSignUp


## Sign in a user
    Amplify.Auth.signIn(
    "username",
    "password",
    result -> Log.i("AuthQuickstart", result.isSignInComplete() ? "Sign in succeeded" : "Sign in not complete"),
    error -> Log.e("AuthQuickstart", error.toString())
     );



## Sign in with web UI
- amplify update auth answer the question 
- run amplify push
- Update AndroidManifest.xml
- Add Response Handler

- Launch Web UI Sign In

      Amplify.Auth.signInWithWebUI(
         this,
        result -> Log.i("AuthQuickStart", result.toString()),
        error -> Log.e("AuthQuickStart", error.  toString())
      );



# Guest access
Follow these steps to enable guest access on your Auth category:

     amplify update auth
       What do you want to do? Walkthrough all the auth configurations
     Select the authentication/authorization services that you want to use: [choose whatever you initially selected - default is User Sign-Up, Sign-In, connected with AWS IAM controls]
     Allow unauthenticated logins? (Provides scoped down permissions that you can control via AWS IAM)
     ❯ Yes
       No
       I want to learn more.

       [proceed through the rest of the steps choosing the values you want - default is usually "No"]



- amplify push

## User attributes
Invoke the following to get the list of attributes assigned to the user

      Amplify.Auth.fetchUserAttributes(
    attributes -> Log.i("AuthDemo", "User attributes = " + attributes.toString()),
    error -> Log.e("AuthDemo", "Failed to fetch user attributes.", error)
      );
- Update user attribute by call updateUserAttribute
- Verify user attribute
- Resend verification code
## Sign out

    Invoke the signOut api
    Amplify.Auth.signOut(
    () -> Log.i("AuthQuickstart", "Signed out successfully"),
         error -> Log.e("AuthQuickstart", error.toString())
     );