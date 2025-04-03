require_relative '../WCSOnboarding/node_modules/react-native/scripts/react_native_pods'

platform :ios, '12.0'

target 'YourAppTarget' do
  use_frameworks!

  use_react_native!(
    path: '../WCSOnboarding',
    fabric_enabled: false,
    hermes_enabled: false
  )

  pod 'WCSOnboarding', :path => '../WCSOnboarding'
end
