
<p align="center">
  <a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="150" src="./asset/logo.png" alt="iotsnackbox.io">
  </a>
  <br>
  <a href="iotsnackbox.io"><img src="https://www.ardu-badge.com/badge/iotsnacksbox_server.svg?version=1.0.1" alt="Build Status">
  </a>
</p>

<h2 align="center">IoT Snacksbox API documantaion for Arduino, Esp32, Esp8266, Raspberry pi.
</h2>

<br>
<p align="center">This api will help you to communicate with the iotsnackbox.io IoT server. Will help control any component from the server. Will help to send any data from the device to the server. Basically it will be helpful for HTTP GET POST.
</p>
<br>
<br>

⚠️ This api will only work in [iotsnackbox.io](https://iotsnacksbox.io/) environment.🙂 

<br>

**What is iotsnacks box?**
<br>
<blockquote> IoT snacks box is an integrated hardware and software platform to deliver end-to-end IoT solutions. Using this device and platform, data can remotely monitor & control by automate processes through IoT.
</blockquote>
<br>

**What types of work can be done by iotsnacksbox?**
<br>
<blockquote>
Automate processes for  agriculture, industry automation, energy control, healthcare, datalogging and any other system that  can be solved using IoT. With the latest technology and user engaging user experience design with the  finest architecture our web platform allows users to deploy cloud IoT applications, control & monitor  dashboards with any IoT devices. 
</blockquote>
<br>

**iotsnacksbox for whom?**
<br>
<blockquote>
This development board provides a range of features that allow developers to build advanced application for smart home, education purpose, gardening, security system specially industrial automation and agricultural sectors.
</blockquote>
<br>
<br>



## Usage And Examples ##

**Request Type:**
<br>
```
HTTP Request.
  ├── 1.0. HTTP Get Request.
  │   ├── 1.1. HTTP Get Request for Single Action.
  │   └── 1.2. HTTP Get Request for Multiple Actions.
  └── 2.0. HTTP Post Request.
      ├── 2.1.HTTP Post Request for Single Triger.
      ├── 2.1.HTTP Post Request for Multiple Trigers.
      ├── 2.1.HTTP Post Request for Single Action.
      └── 2.1.HTTP Post Request for Multiple Actions.
```
<br>

**widgets Type:**
<br>
```
widgets
  ├── 1.0. Action.
  │   ├── 1.1. On/Off Switch.
  │   ├── 1.2. Slider Switch.
  │   └── 1.3. Selection Switch.
  └── 2.0. Triger
      ├── 2.1. Field Value.
      ├── 2.2. pi Chart.
      ├── 2.3. Bar Chart.
      ├── 2.4. Line Chart.
      └── 2.5. Area Chart.
```

**1.0. GET Request**
<br>
<blockquote>
 GET is used to retrieve and request data from a specified resource in a server. GET is one of the most popular HTTP request techniques. In simple words, the GET method is used to retrieve whatever information is identified by the Request-URL. In case, when you send a GET Request() to the IoT Snacks Box Server, it sends back to you it's (Switch/Slider/Selection Switch/Action) position. Like it’s on/off or its position.
</blockquote>

<br>

**1.1. Get Request for Single Action/Switch :**
<br>
*How it works :*
<a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="100%" src="./asset/GET Request for Action 1.jpg" alt="iotsnackbox.io">
  </a>


*api Description :*

<a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="100%" src="./asset/capture1.PNG" alt="iotsnackbox.io"></a>
 When you want to use this api don't need change anything just change Toke number of your project insted "abc123***"

 ⚠️ Don't share your Token number.
 <br>
 <br>

*api Link :*
```
https://api.iotsnacksbox.io/actions?snacksboxtoken=abc123******

```
*Json :*
```
[
  {
    "values":[0,1],
    "_id":"60362063c8aa795ca696e6c0",
    "name":"Relay1",
    "type":"Boolean",
    "value":"0",
    "createdAt":"2021-02-24T09:46:11.173Z",
    "updatedAt":"2021-02-24T09:46:11.173Z"
  }
]
```


Example Code for [Arduino](#), [ESP32](#), [Raspberry pi](#).

<br>

**1.2. Get Request for Multiple Actions/Switch:**
<br>

*api Description :*

<a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="100%" src="./asset/capture1.PNG" alt="iotsnackbox.io"></a>
 When you want to use this api don't need change anything just change Toke number of your project insted "abc123***"

 ⚠️ Don't share your Token number.
 <br>
 <br>

*api Link :*
```
https://api.iotsnacksbox.io/actions?snacksboxtoken=b0e504366******

```


*Json :*
```
[
  {
    "values":[0,1],
    "_id":"60362063c8aa795ca696e6c0",
    "name":"Relay1",
    "type":"Boolean",
    "value":"0",
    "createdAt":"2021-02-24T09:46:11.173Z",
    "updatedAt":"2021-02-24T09:46:11.173Z"
  },
  {
    "values":[0,1],
    "_id":"60362063c8aa795ca696e6c1",
    "name":"Relay2",
    "type":"Boolean",
    "value":"1",
    "createdAt":"2021-02-24T09:46:11.173Z",
    "updatedAt":"2021-02-24T09:46:11.173Z"
  }
]
```


Example Code for [Arduino](#), [ESP32](#), [Raspberry pi](#).

<br>

**2.0. POST Request**
<br>
<blockquote>
 POST Request: In web communication, POST requests are utilized to send data to a server to create or update a resource.  The information submitted to the server with POST request method is archived in the request body of the HTTP request. The HTTP POST method is often used to send user-generated data to a server. One example is when a user uploads a profile photo. If you want to see your data in IoT server in different widgets (Field value /Pi chart /Line chart/Bar chart/Area Chart), you need to send a POST Request() with your data like (Temperature : 30°C, Light : 220lm).
</blockquote>
<br>

**2.1. Post Request for Single Triger/Sensor:**
<br>

*How it works :*
<a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="100%" src="./asset/Post Request for trigger 1.jpg" alt="iotsnackbox.io">
  </a>


*api Description :*

<a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="100%" src="./asset/capture2.PNG" alt="iotsnackbox.io"></a>
 When you want to use this api don't need change anything just change Toke number of your project insted "abc123***"

 ⚠️ Don't share your Token number.
 <br>
 <br>

*api Link :*
```
https://api.iotsnacksbox.io/trigger/temperature?snacksboxtoken=ab12***


```
*Json :*
```
{
  "data":
  {"Temperature":27}
}
```


Example Code for [Arduino](#), [ESP32](#), [Raspberry pi](#).

<br>

**2.2. Post Request for Multiple Triger/Sensors:**
<br>

*api Description :*

<a href="iotsnackbox.io" target="_blank" rel="noopener noreferrer"><img width="100%" src="./asset/capture3.PNG" alt="iotsnackbox.io"></a>
 When you want to use this api don't need change anything just change Toke number of your project insted "abc123***"

 ⚠️ Don't share your Token number.
 <br>
 <br>

*api Link :*
```
https://api.iotsnacksbox.io/trigger/weather?snacksboxtoken=abc123***
```
*Json :*
```
{
  "data":
    {
      "Temperature":59,
      "Humidity":105,
      "Light":84,
      "Smoke":21
    }
  }
```


Example Code for [Arduino](#), [ESP32](#), [Raspberry pi](#).

<br>

**2.1.HTTP Post Request for Single Action:**
<br>

Server Setup:
api Link:
api Description:
Json Type:
Json Description:
Code for arduino, esp32,raspberry pi.

<br>

**2.1.HTTP Post Request for Multiple:**
<br>

Server Setup:
api Link:
api Description:
Json Type:
Json Description:
Code for arduino, esp32,raspberry pi.

<br>



 



 # Overview #

 # Feature #

