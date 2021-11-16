# RecyclerView
The RecyclerView class extends the ViewGroup class and implements ScrollingView interface. It is introduced in Marshmallow. It is an advanced version of the ListView with improved performance and other benefits.
- RecyclerView is mostly used to design the user interface with the fine-grain control over the lists and grids of android application.
- A flexible view for providing a limited window into a large data set.

- when we create view holder (the element in the list) it dosnt have   we use RecyclerView like this data RecyclerView.ViewHolder to connect it with data the RecyclerView use adapter to do that
## How does RecyclerView work?
RecyclerView does not allocate an item view for every item in your data source. Instead, it allocates only the number of item views that fit on the screen(Viewport) and it reuses those item layouts as the user scrolls. ... When a view scrolls out of sight and is no longer displayed, it becomes a scrap view .
## Plan your layout:
Items in your RecyclerView are arranged by a LayoutManager class. The RecyclerView library provides three layout managers:
- LinearLayoutManager arranges the items in a one-dimensional list
- GridLayoutManager arranges all items in a two-dimensional grid
- StaggeredGridLayoutManager the item not same high or width. The result is that the items in a row or column can end up offset from each other.
## Implementing your adapter and view holder
we said we need adapter so When you define your adapter, you need to override three key methods:

1. onCreateViewHolder():  calls  when to create a new ViewHolder it initializes the ViewHolder and its associated View, but does not fill in the view's contents.

        @Override
    public ViewHolder onCreateViewHolder(ViewGroup viewGroup, int viewType) {
        // Create a new view, which defines the UI of the list item
        View view = LayoutInflater.from(viewGroup.getContext())
                .inflate(R.layout.text_row_item, viewGroup, false);

        return new ViewHolder(view);
    }

2. onBindViewHolder():  calls to associate a ViewHolder with data. The method fetches the appropriate data and uses the data to fill in the view holder's layout.

       @Override
         public void onBindViewHolder(ViewHolder viewHolder, final int position) {
        viewHolder.getTextView().setText(localDataSet[position]);
         }


3. getItemCount():  calls  to get the size of the data set. 

      @Override
    public int getItemCount() {
        return localDataSet.length;
    }
