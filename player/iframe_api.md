# Using Player IFrame API

Player utilizes HTML5 postMessage API. Please note that this feature will not work correctly on older browsers like IE8.

## Methods

You can send message object to player window containing following mandatory fields:

* `method` - Method name according Player API reference
* `params` - Parameters array ordered by their precedence according Player API reference

### Example

    var w = document.getElementById('player').contentWindow
    w.postMessage({method: "volume", params: [0.5]}, "*")

## Reading method response

Due to asynchronous way of calling methods throught window postMessage you have to listen to resulting message.

Object passed to window has the following structure:

* `method` - Event name according Player API reference
* `result` - Result of method

### Example

    window.addEventListener("message", receiveMessage, false);
    
    function receiveMessage(message){
  
      var method = message.data.method;
      var result = message.data.result;
      
      console.log(method);
      console.log(result);
  
    }

## Events

Player will send all events using the same technique but in the reverse direction to parent frame.

Object passed to window has the following structure:

* `event` - Event name according Player API reference
* `params` - Parameters array ordered by their precedence according Player API reference

### Example

    window.addEventListener("message", receiveMessage, false);
    
    function receiveMessage(message){
  
      var event = message.data.event;
      var params = message.data.params;
      
      console.log(event);
      console.log(params);
  
    }
