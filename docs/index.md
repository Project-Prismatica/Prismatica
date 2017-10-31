The Prismatica project is dedicated to having your cake and eating it too.

![Screenshot]({{ site.url }}/screenshot.png)



## Simple REACTJS Beacon

```js
// Defining a BeaconHandler Class
var BeaconHandler = React.createClass({
  loadCommandsFromServer: function() {
    $.ajax({
      url: this.props.url,
      dataType: 'json',
      cache: false,
      success: function(data) {
        this.setState({data: data});
      }.bind(this),
      error: function(xhr, status, err) {
        console.log(this.props.url, status, err.toString());
      }.bind(this)
    });
  },
  getInitialState: function() {
    return {data: []};
  },
  componentDidMount: function() {
    this.loadCommandsFromServer();
    setInterval(this.loadCommandsFromServer, this.props.pollInterval);
  },
  //Push tasks to execution
  render: function() {
   return (
     <Exec data = {this.state.data} />
   );
  }
});
```

```
![Screenshot]({{ site.url }}/hills.png)
```
