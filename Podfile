platform :ios, '15.0'

project 'MyBrowserApp.xcodeproj'

target 'MyBrowserApp' do
  use_frameworks!
  # 의존성 추가 가능: 예) pod 'Alamofire', '~> 5.6'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.resources_build_phase.files.each do |file|
      if file.display_name.include?("PrivacyInfo.xcprivacy")
        file.remove_from_project
      end
    end
  end
end