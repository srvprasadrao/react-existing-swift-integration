# react-existing-swift-integration
Follwed steps as mentioned here https://facebook.github.io/react-native/docs/integration-with-existing-apps.html

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

Tech stack
------------
Swift appliacation : Swift-4
iOS version: 11.3
XCode: 9.3

DoubleConversion (1.1.5)
Folly (2016.09.26.00)
React (0.55.2)
boost-for-react-native (1.63.0)
glog (0.3.4)
yoga (0.55.2.React)
