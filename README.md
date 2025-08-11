## How To Install

1. **Edit Your Podfile** (inside `ios/Podfile`):

   ```ruby
   target 'YourApp' do
     # Add these lines above `pod install`:
     pod 'adriano-rodrigues99-ffmpeg-kit-ios', :podspec => 'https://raw.githubusercontent.com/adriano-rodrigues99/ffmpeg/master/adriano-rodrigues99-ffmpeg-kit-ios.podspec'
     pod 'ffmpeg-kit-react-native', :path => '../node_modules/ffmpeg-kit-react-native'

     # ...other pods
   end
   ```

2. **Modify `ffmpeg-kit-react-native.podspec`** in `node_modules/ffmpeg-kit-react-native`:

```ruby
require "json"

package = JSON.parse(File.read(File.join(__dir__, "package.json")))

Pod::Spec.new do |s|
  s.name         = package["name"]
  s.version      = package["version"]
  s.summary      = package["description"]
  s.homepage     = package["homepage"]
  s.license      = package["license"]
  s.authors      = package["author"]

  s.platform          = :ios
  s.requires_arc      = true
  s.static_framework  = true

  s.source       = { :git => "https://github.com/arthenica/ffmpeg-kit.git", :tag => "react.native.v#{s.version}" }
  s.default_subspec = 'https' # Just change to whatever subspec you want to use, e.g 'min-gpl'
  s.dependency "React-Core"

  s.subspec 'min' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'min-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'min-gpl' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'min-gpl-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'https' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'https-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'https-gpl' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'https-gpl-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'audio' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'audio-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'video' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'video-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'full' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'full-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'full-gpl' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end

  s.subspec 'full-gpl-lts' do |ss|
      ss.source_files      = '**/FFmpegKitReactNativeModule.m',
                            '**/FFmpegKitReactNativeModule.h'
      ss.dependency 'adriano-rodrigues99-ffmpeg-kit-ios', "6.0.2"
      ss.ios.deployment_target = '12.1'
  end
end
```

#### If using Expo Dev just run:

```bash
expo prebuild --clean
```

#### For bare native apps

3. **Install Pods**:

   ```bash
   cd ios
   pod install --repo-update
   ```

4. **Clean & Rebuild** if needed:

   ```bash
   rm -rf Pods Podfile.lock
   pod install --repo-update
   ```

5. **Done** — Now iOS uses your custom FFmpeg Pod (`adriano-rodrigues99-ffmpeg-kit-ios`) via `ffmpeg-kit-react-native`.

## (Optional Step To Persist Changes) Patching `ffmpeg-kit-react-native` with `patch-package`

1. **Install `patch-package`:**

   ```bash
   npm install --save-dev patch-package
   ```

2. **Add a Postinstall Script** in your `package.json`:

   ```json
   {
     "scripts": {
       "postinstall": "patch-package"
     }
   }
   ```

3. **Edit the Package**:

   - Go to `node_modules/ffmpeg-kit-react-native/ffmpeg-kit-react-native.podspec`
   - Make your changes (e.g., pointing to custom FFmpeg Pods).

4. **Generate the Patch**:

   ```bash
   npx patch-package ffmpeg-kit-react-native
   ```

   This creates a patch file in `patches/`.

5. **Commit the Patch**:
   - Add and commit the `.patch` file in `patches/`.
   - Now every time you install dependencies, your changes are automatically re-applied.

## [Expo] Adding a Config Plugin for Custom FFmpeg Pods

1. **Create `with-ffmpeg-pod.js`** at your project root:

   ```js
   const {
     withPlugins,
     createRunOncePlugin,
     withDangerousMod,
   } = require("@expo/config-plugins");
   const fs = require("fs");
   const path = require("path");

   function addPodDependency(podfilePath) {
     const podInstallLine = `pod 'adriano-rodrigues99-ffmpeg-kit-ios', :podspec => 'https://raw.githubusercontent.com/adriano-rodrigues99/ffmpeg/master/adriano-rodrigues99-ffmpeg-kit-ios.podspec'`;
     const podInstallLine2 = `pod 'ffmpeg-kit-react-native', :path => '../node_modules/ffmpeg-kit-react-native'`;

     let contents = fs.readFileSync(podfilePath, "utf8");
     if (!contents.includes(podInstallLine)) {
       contents = contents.replace(
         /post_install do \|installer\|/g,
         `${podInstallLine}\n\n  post_install do |installer|`
       );

       contents = contents.replace(
         /post_install do \|installer\|/g,
         `${podInstallLine2}\n\n  post_install do |installer|`
       );

       fs.writeFileSync(podfilePath, contents, "utf8");
     }
   }

   function withMyFFmpegPod(config) {
     return withDangerousMod(config, [
       "ios",
       (cfg) => {
         const podfilePath = path.join(
           cfg.modRequest.platformProjectRoot,
           "Podfile"
         );
         addPodDependency(podfilePath);
         return cfg;
       },
     ]);
   }

   const withFFmpegPod = (config) => {
     return withPlugins(config, [withMyFFmpegPod]);
   };

   module.exports = createRunOncePlugin(
     withFFmpegPod,
     "with-ffmpeg-pod",
     "1.0.0"
   );
   ```

2. **Reference the Plugin** in your `app.json`:

```json
{
  "expo": {
    "name": "MyApp",
    "plugins": [
      ["@config-plugins/ffmpeg-kit-react-native"], // This npm package should be installed
      "./plugins/with-ffmpeg-pod.js"
    ]
  }
}
```

_(If you’re using `app.config.js`, add `plugins: ["./with-ffmpeg-pod.js"]` in the exported config.)_

3. **Prebuild and Install**:
   ```bash
   expo prebuild -p ios
   cd ios
   pod install
   ```
   The generated `Podfile` will now include:
   ```ruby
   pod 'adriano-rodrigues99-ffmpeg-kit-ios', :podspec => '...'
   pod 'ffmpeg-kit-react-native', :path => '../node_modules/ffmpeg-kit-react-native'
   ```

That’s it! Your Expo project will automatically inject the custom Pods each time you run `expo prebuild`, keeping your iOS setup in sync with your custom FFmpeg binaries.
