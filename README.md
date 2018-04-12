# react-existing-swift-integration
Follwed steps as mentioned here https://facebook.github.io/react-native/docs/integration-with-existing-apps.html

I did below steps to resolve this but stuck in Issue-4

`../node_modules/react-native`
Fetching podspec for `glog` from `../node_modules/react-native/third-party-podspecs/glog.podspec`
Fetching podspec for `yoga` from `../node_modules/react-native/ReactCommon/yoga`
Downloading dependencies
Installing DoubleConversion (1.1.5)
Installing Folly (2016.09.26.00)
Installing React (0.55.2)
Installing boost-for-react-native (1.63.0)
Installing glog (0.3.4)
Installing yoga (0.55.2.React)
Generating Pods project
Integrating client project

[!] Please close any current Xcode sessions and use `SwiftHelloWorld.xcworkspace` for this project from now on.
Sending stats
Pod installation complete! There are 10 dependencies from the Podfile and 6 total pods installed.

Issue-1
--------
'algorithm' file not found

solution: add below to yoga.podspec file

# Only expose the needed headers
  spec.public_header_files = 'yoga/Yoga.h', 'yoga/YGEnums.h', 'yoga/YGMacros.h'

Issue-2
--------
'folly/folly-config.h' file not found

Solution: add these files to exclude list in React.podspec
            "React/Fabric/*",

Issue-3
-------
'fishhook/fishhook.h' file not found

Solution: change fishhook to React

Issue-4
-------
Could not build Objective-C module 'React'
