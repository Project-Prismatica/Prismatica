The Prismatica project is dedicated to having your cake and eating it too.

## Prismatica Application Marketplace  

- [Prism Launcher]() The package manager for Prism Apps (Releasing at WWHF) 
- [Prism Project Manager]() Project management, findigns, and reporting tool (Releasing at WWHF) 
- [Diagon](https://github.com/Project-Prismatica/Diagon) A Command and Control Toolkit 
- [Acheron](https://github.com/Acheron-VAF/Acheron) Acheron is a RESTful vulnerability assessment and management framework built around search and dedicated to terminal extensibility. (Releasing at WWHF)
- [Tiberium](https://github.com/0sm0s1z/Tiberium/releases) A Command and Control scanning tool


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


![Screenshot]({{ site.url }}/hills.png)
