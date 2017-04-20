# ionic

`Steps for creating ionic app `

`Step 1: Install `<a href="https://nodejs.org/en/" traget="_blank"> Node.js</a>

`Step 2: Install the latest Cordova and Ionic command-line tools `

`Cmd: npm install -g cordova ionic `

`Step 3: Install Sample Project `

`Cmd: ionic start myFirstApp tabs `

`Step 4: process to run project`

`Cmd: cd myFirstApp`

`Cmd: ionic platform add Android`

`Cmd: ionic build Android`

`Cmd: ionic emulate Android`

`Step 5: Run Ionic project in browser `

`Cmd: ionic serve `
`or`
`Cmd: ionic serve -l`



# Install Network information cordova plugin

`Cmd: cordova plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-network-information.git`

`Update Code In app.js file`

`.run(function($ionicPlatform, $ionicPopup) {
  $ionicPlatform.ready(function() {

    // Check for network connection
    if(window.Connection) {
      if(navigator.connection.type == Connection.NONE) {
        $ionicPopup.confirm({
          title: 'No Internet Connection',
          content: 'Sorry, no Internet connectivity detected. Please reconnect and try again.'
        })
        .then(function(result) {
          if(!result) {
            ionic.Platform.exitApp();
          }
        });
      }
    }

  });`
