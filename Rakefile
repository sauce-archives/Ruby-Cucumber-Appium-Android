def run_tests(deviceName, platformName, platformVersion, app)
  system("deviceName=\"#{deviceName}\" platformName=\"#{platformName}\" platformVersion=\"#{platformVersion}\" app=\"#{app}\" parallel_cucumber features -n 20")
end

task :Galaxy_S7_Device do
  run_tests('Samsung Galaxy S7 WQHD GoogleAPI Emulator', 'Android', '7.1', 'http://saucelabs.com/example_files/ContactManager.apk')
end

task :Galaxy_S4_Emulator do
  run_tests('Samsung Galaxy S4 Emulator', 'Android', '4.4', 'http://saucelabs.com/example_files/ContactManager.apk')
end

multitask :test_sauce => [
    :Galaxy_S7_Device,
    :Galaxy_S4_Emulator

  ] do
    puts 'Running automation'
end
