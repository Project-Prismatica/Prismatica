The Prismatica project is dedicated to having your cake and eating it too.

## Getting Started

To get started with Prismatica you will need to spin up an Emergence server to bind all subcomponents together across a shared data model. Emergence servers can be spun up quickly using Docker. Alternately, it can be executed manually using the `npm install` and `npm start` commnads. To run Emergence within a Docker container the `docker` and `docker-compose` commands must be installed. Installing Docker:

On Windows: https://docs.docker.com/docker-for-windows/install/

On Linux:
```
apt install docker.io
apt install docker-compose
```

Run Emergence:
```
git clone https://github.com/Project-Prismatica/Emergence.git
cd Emergence
docker-compose up
```

Now that Emergence is running you are ready to start up Prism Apps! Diagon and Oculus are a good place to start.

Installing Diagon:

Diagon can be downloaded at the following link: [Diagon](https://github.com/Project-Prismatica/Diagon)

![Screenshot]({{ site.url }}/screenshot.gif)

You will need to configure the Diagon settings with the IP address of the system where Emergence is running. Then to setup listeners you will need to run Oculus.

Installing Oculus:

```
git clone https://github.com/Project-Prismatica/Oculus.git
cd Oculus
python oculus.py
```

Now you're all ready to rock and roll! Happy Hacking!

## Prismatica Application Marketplace

- [Diagon](https://github.com/Project-Prismatica/Diagon) The Diagon Attack Framework is a Prismatica application containing the Ravenclaw, Gryffindor, and Slytherin remote access tools (RATs).
- [Emergence](https://github.com/Project-Prismatica/Emergence) The Emergence fabric is an interface where interaction and integration of disparate information security subsystems gain combined intelligence.
- [Oculus](https://github.com/Project-Prismatica/Oculus) Oculus is a malleable python-based C2 system allowing for instantiation of listeners for the purpose of communication with remote access tools (RATs).
- [Prism Launcher]() The package manager for Prism Apps (Releasing at WWHF)
- [Prism Project Manager]() Project management, findigns, and reporting tool (Releasing at WWHF)
- [Acheron](https://github.com/Acheron-VAF/Acheron) Acheron is a RESTful vulnerability assessment and management framework built around search and dedicated to terminal extensibility.
- [Tiberium](https://github.com/0sm0s1z/Tiberium/releases) A Command and Control scanning tool


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
