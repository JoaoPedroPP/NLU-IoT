# Iot-with-Bot`s

This is the official repository with all code used By Eduardo Petecof and João Pedo P.P during their lecture about how to integrate IoT devices with Chatbots using IBM Cloud.

If you want to reproduce this lecture first thing you need to do s create an acount in [IBM Cloud](https://bluemix.net)

## Functions

In this folder you will find the actions that are executed when the bot identifier some command that the iot device should excute.

Inside its there are two folders, one for the NodeMCU+ESP2866 device and other for the Omega.

Functions are pieces of code hosted in IBM Cloud that you can call to perform an action though an http request.

Example of function:

```javascript
function main(param){
    if (param.example != undefined) return {msg: param.example}
    else return {msg: 'param is null'}
}
```

Example of param

```josn
{
    example: "Hello Wordl",
    example01: 23,
    example02:{
        inside01:32,
        inside02: "Inside Wordl"
    }
}
```

## Device code

This folder contains all files used in each device to connect to IBM IoT Platform and perform the required actions.

### NodeMCU Files
![NodeMCU](/Img/NodeMCU.jpeg)

### Omega2+ Files
![Omega2+Img](/Img/Omega2.jpeg)

[Omega2+](http://onion.io) is development board with a linux kernel inside specifically designed for IoT applications, according to the maker "World's smallest Linux server".

His linux kernel allows its to run any programming languages, in this specifaclly project is was used Node.js to connect and perform the commands sent by the IoT Platform.

If you have an Omega2+ or some development board similar you just need to copy the content of the Omega`s folder to your board and follow the next steps:
1. run `npm install`;
2. fufill the .env file with your IoT credentials and save
   ```env
   IOT_ORG=<YOUR_IOT_ORG_HERE>
   IOT_DEVICE_TYPE=<YOUR_IOT_DEVICE_TYPE>
   IOT_AUTH_KEY=<YOUR_IOT_AUTH_KEY>
   IOT_AUTH_TOKEN=<YOUR_IOT_AUTH_TOKEN>
   ```
3. run `npm start`

### Mobile app

## Contributors
* [Eduardo Petecof Mattoso](https://github.com/epetecof)
* [Joao Pedro Poloni Ponce](https://github.com/JoaoPedroPP)

## Special Thanks
* [Danilo Paschon](https://www.linkedin.com/in/danilo-paschon/) -> without him there will be no project
  

![Node+Omega](/Img/MCU+Omega.jpeg)