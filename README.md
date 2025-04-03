react_native_path = '../WCSOnboarding/node_modules/react-native'

target 'YourAppTarget' do
  use_frameworks!

  # 🔗 Zależności React Native – podajesz ręcznie, bo nie ma node_modules
  pod 'React-Core', :path => react_native_path
  pod 'React-RCTBridge', :path => react_native_path
  pod 'React-RCTView', :path => react_native_path
  pod 'React-RCTText', :path => react_native_path
  pod 'React-CoreModules', :path => react_native_path

  # 🧩 Twój pod
  pod 'WCSOnboarding', :path => '../WCSOnboarding'
end
