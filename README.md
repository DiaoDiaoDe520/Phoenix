# Phoenix
just Phoenix


platform :ios, '10.2'
target 'Perfect' do

use_frameworks!

  pod 'RealmSwift'
  pod 'SwiftLint'
  pod 'ChameleonFramework/Swift', :git => 'https://github.com/ViccAlexander/Chameleon.git'
  pod 'SnapKit'
  pod 'SwiftDate'
  pod 'JPush'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '3.0'
    end
  end
end
