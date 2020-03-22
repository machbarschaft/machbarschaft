<img src="https://github.com/marc-sommer/machbarschaft/blob/master/machbarschaft-logo.jpeg" height="160px" width="auto">

## What is it?
Machbarschaft is a project that has been created while <a href="https://wirvsvirushackathon.org/">WirVsVirus hackathon</a> which took part from 20.03.2020 to 22.03.2020. 
The aim of this project is providing help for people which have to stay at home in quarantine and have no access to the internet. For those people we have created Machbarschaft. It is a phone number that people can call. Here they can provide information what they need, how urgent this work is and personal information. Those data is collected and provided in an app where other users see those orders. They can get in touch with those people and fulfil this order so that the caller has not to leave his house or apartment.

## How does it work?
1. A person who needs help calls a german phone number (which is located in Hamburg) that is configured and hosted with Twilio
2. The data is collected with Twilio and is sent to a Google Cloud function webservice
3. This webservice transforms the data, gets the location for the address (longitude, latitude) and stores it in a Firebase database as an order
4. The apps for iOS and Android request those orders. There those orders are displayed in a map from Google Maps. Furthermore they are displayed in a list.
5. A helper clicks onto an order in the list and calls the person who needs help for getting more information, e.g. for a purchase which products are needed
6. The helper fulfils this actions and got paid by the caller

### How to test it?
Just feel free to test our nice bot Lisa which answers your request: <a href="tel:+4940299960980">+49 40 2999 60980</a>
Your request will be processed and stored in our database.

### Repositories
The project is structured in several parts. The repository for every single part of the application is listed in the following table. Here you can get more information in detail how this part of the application works and access the source code.

| Repository  | GitHub-Link | Contributors | 
| ------------- | ------------- | ----------- |
| iOS App | https://github.com/marc-sommer/machbarschaft-ios |<a href="https://github.com/felixschlegel">felixschlegel</a><br/><a href="https://github.com/LinusGeffarth ">LinusGeffarth</a><br/><a href="https://github.com/packatino">packatino</a><br/><a href="https://github.com/DEOA ">DEOA</a><br/><a href="https://github.com/marc-sommer">marc-sommer</a>|
| Android-App  | https://github.com/Basler182/einanrufhilft_application |<a href="https://github.com/moonlight200">moonlight200</a><br/><a href="https://github.com/Basler182">Basler182</a><br/><a href="https://github.com/bene99">bene99</a><br/><a href="https://github.com/JulianWieners">JulianWieners</a><br/><a href="https://github.com/alexanderhodes">alexanderhodes</a>|
| Google Cloud Function | https://github.com/dvs23/machbarschaft-firebase-api |<a href="https://github.com/dvs23">dvs23</a><br/><a href="https://github.com/joterr">joterr</a><br/><a href="https://github.com/alexanderhodes">alexanderhodes</a>|
| Twilio configuration | https://github.com/alexanderhodes/machbarschaft-twilio |<a href="https://github.com/dvs23">dvs23</a><br/><a href="https://github.com/joterr">joterr</a><br/><a href="https://github.com/alexanderhodes">alexanderhodes</a>|
| Website | https://github.com/marc-sommer/machbarschaft-web |<a href="https://github.com/code-lukas">code-lukas</a><br/><a href="https://github.com/marc-sommer">marc-sommer</a>|
| Design | https://github.com/marc-sommer/machbarschaft-design | <a href="https://github.com/marc-sommer">marc-sommer</a><br/><a href="https://github.com/Keja0809">Keja0809</a><br/>|

#### Architecture

<img src="https://github.com/marc-sommer/machbarschaft/blob/master/architecture.png" alt="Architecture" height="500px" width="auto">

#### Techstack
- iOS App: Swift
- Android App: Java
- Google Cloud function: JavaScript
- Website: HTML, CSS, JavaScript
- Further things: JSON for data exchange, Firebase Functions, Firebase Authentication, Firebase Storage, Firebase Database, Twilio, Google Maps API

#### Further ressources
- <a href="https://www.figma.com/file/qMwnqgj0VtgbHztbnhM8lq/%23einanrufhilft">Figma resources</a>
- <a href="https://machbarschaft.jetzt/">Machbarschaft Homepage</a>
- GitHub Repositories in the upper table

#### Contributors
<table>
  <tr>
    <td align="center">
      <a href="https://github.com/marc-sommer/">
        <img src="https://avatars3.githubusercontent.com/u/30161952?s=460&u=61859c693e76cc3a8ef7a34940ba8f60e3f8b1fe&v=4" width="100px;" alt=""><br/>
        <sub><b>Marc</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/Basler182/">
        <img src="https://avatars3.githubusercontent.com/u/48420258?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Kilian</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/moonlight200/">
        <img src="https://avatars2.githubusercontent.com/u/9433312?s=460&u=2cbd3b455e0b874b3c1ae17547c1ad3c5a1539b6&v=4" width="100px;" alt=""><br/>
        <sub><b>Felix</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/bene99/">
        <img src="https://avatars2.githubusercontent.com/u/53974702?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Benedikt</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/JulianWieners/">
        <img src="https://avatars3.githubusercontent.com/u/42766946?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Julian</b></sub>
      <a/>
    </td>
  </tr>
  <tr>
     <td align="center">
      <a href="https://github.com/dvs23/">
        <img src="https://avatars0.githubusercontent.com/u/5659161?s=460&u=fa462c5f56c733bc9cfc6f9f77b844ac95f0fa51&v=4" width="100px;" alt=""><br/>
        <sub><b>David</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/code-lukas/">
        <img src="https://avatars3.githubusercontent.com/u/57943620?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Lukas</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/felixschlegel/">
        <img src="https://avatars1.githubusercontent.com/u/26013286?s=460&u=c9b8afae9edc835b8085934550eb9780c6eb7619&v=4" width="100px;" alt=""><br/>
        <sub><b>Felix</b></sub>
      <a/>
    </td>
      <td align="center">
      <a href="https://github.com/joterr/">
        <img src="https://avatars1.githubusercontent.com/u/30891111?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Jannik</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/alexanderhodes/">
        <img src="https://avatars3.githubusercontent.com/u/17107309?s=460&u=36b2d212c652f9d1537ad685b3b3d759d0013290&v=4" width="100px;" alt=""><br/>
        <sub><b>Alex</b></sub>
      <a/>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/LinusGeffarth">
        <img src="https://avatars2.githubusercontent.com/u/9455439?s=460&u=42cda172fb5b4dc5c5d0bb972f1c069bbd1d8e93&v=4" width="100px;" alt=""><br/>
        <sub><b>Linus</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/packatino/">
        <img src="https://avatars2.githubusercontent.com/u/6194284?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Robert</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/DEOA/">
        <img src="https://avatars0.githubusercontent.com/u/21275941?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>DEOA</b></sub>
      <a/>
    </td>
    <td align="center">
      <a href="https://github.com/Keja0809">
        <img src="https://avatars1.githubusercontent.com/u/22995330?s=460&v=4" width="100px;" alt=""><br/>
        <sub><b>Keja0809</b></sub>
      <a/>
    </td>
  </tr>
</table>
