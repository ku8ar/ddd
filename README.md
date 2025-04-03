Pod::Spec.new do |s|
  s.name         = 'RNModule'
  s.version      = '1.0.0'
  s.summary      = 'React Native module as CocoaPod'
  s.description  = 'React Native feature module integrated via CocoaPods.'
  s.homepage     = 'https://example.com'
  s.license      = 'MIT'
  s.author       = { 'You' => 'you@example.com' }
  s.source       = { :path => '.' }

  s.platform     = :ios, '11.0'
  s.source_files = 'ios/RNModule/**/*.{h,m}'

  s.requires_arc = true
  s.dependency 'React-Core'
  s.dependency 'React-RCTView'
  s.dependency 'React-RCTBridge'
  s.dependency 'React-RCTText'
  s.dependency 'React-CoreModules'

  s.pod_target_xcconfig = {
    'DEFINES_MODULE' => 'YES',
    'SWIFT_VERSION' => '5.0'
  }
end




npx react-native bundle \
  --platform ios \
  --entry-file index.js \
  --bundle-output ios/RNModule/main.jsbundle \
  --assets-dest ios/RNModule
