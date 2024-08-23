# gwm-haval-h6-gt-multimidia-native 👀


Accessing the Haval H6 GT vehicle's operating system from GWM, I found the following secrets configs from mycar:


This will be useful for security researchers to update their tools and for professional engineers to debug GWM's code and development your own app.

```bash
:/data # df                                                                                                                                                                                  
Filesystem                           1K-blocks    Used Available Use% Mounted on
/dev/root                              4063212 3039532   1023680  75% /
tmpfs                                  3212636     844   3211792   1% /dev
tmpfs                                  3212636       0   3212636   0% /mnt
/dev/block/dm-1                        1289504  421792    867712  33% /vendor
/dev/block/vdb                        10994724 1760412   9234312  17% /data
/dev/block/vdd                           27632     328     27304   2% /mnt/vendor/persist
/dev/block/vde                          174000   24064    149936  14% /vendor/firmware_mnt
/dev/block/vdf                           65488     112     65376   1% /vendor/bt_firmware
/dev/block/vdh                          499656     404    499252   1% /mnt/user/appcfg
/dev/block/vdi                             488      60       428  13% /mnt/vendor/crypto
/dev/block/vdj                        16382888 3498772  12884116  22% /mnt/user/mapdata
/dev/block/vdk                         2031440  155520   1875920   8% /mnt/user/vrdata
/dev/block/vdm                          999320  105580    893740  11% /mnt/user/logdatabr
tmpfs                                    10240       0     10240   0% /data/ramfs
/data/media                           10994724 1760412   9234312  17% /mnt/runtime/default/emulated
192.168.118.2:/logdata/                1048576  558528    490048  54% /data/nfs/nfs_log
192.168.118.2:/otaupdate/installPkg/   4194304  138656   4055648   4% /data/nfs/nfs_ota
192.168.118.2:/var/log                 1048576   59616    988960   6% /data/nfs/nfs_log/dlt/dump
192.168.118.2:/bvims                   1048576   33600   1014976   4% /data/nfs/nfs_bvims
192.168.118.2:/dvr1                    1033088 1023168      9920 100% /data/nfs/nfs_dvr1
```

```
1|:/data # getprop
[DEVICE_PROVISIONED]: [1]
[af.fast_track_multiplier]: [1]
[audio.deep_buffer.media]: [true]
[audio.offload.buffer.size.kb]: [32]
[audio.offload.gapless.enabled]: [true]
[audio.offload.min.duration.secs]: [60]
[audio.offload.pcm.16bit.enable]: [true]
[audio.offload.pcm.24bit.enable]: [true]
[audio.offload.video]: [true]
[audio.volume.headset.gain.depcal]: [true]
[av.offload.enable]: [true]
[boot.car_service_created]: [1]
[bt.max.hfpclient.connections]: [1]
[com.android.car.radio.demo]: [false]
[config.disable_rtt]: [true]
[dalvik.vm.appimageformat]: [lz4]
[dalvik.vm.dex2oat-Xms]: [64m]
[dalvik.vm.dex2oat-Xmx]: [512m]
[dalvik.vm.dex2oat-minidebuginfo]: [true]
[dalvik.vm.dexopt.secondary]: [true]
[dalvik.vm.heapgrowthlimit]: [96m]
[dalvik.vm.heapmaxfree]: [8m]
[dalvik.vm.heapminfree]: [512k]
[dalvik.vm.heapsize]: [384m]
[dalvik.vm.heapstartsize]: [8m]
[dalvik.vm.heaptargetutilization]: [0.75]
[dalvik.vm.image-dex2oat-Xms]: [64m]
[dalvik.vm.image-dex2oat-Xmx]: [64m]
[dalvik.vm.isa.arm.features]: [default]
[dalvik.vm.isa.arm.variant]: [cortex-a9]
[dalvik.vm.isa.arm64.features]: [default]
[dalvik.vm.isa.arm64.variant]: [generic]
[dalvik.vm.stack-trace-dir]: [/data/anr]
[dalvik.vm.usejit]: [true]
[dalvik.vm.usejitprofiles]: [true]
[debug.atrace.tags.enableflags]: [0]
[debug.egl.hw]: [0]
[debug.force_rtl]: [0]
[debug.mdpcomp.logs]: [0]
[debug.sf.hw]: [0]
[debug.sf.latch_unsignaled]: [1]
[debug.sf.nobootanimation]: [1]
[dev.bootcomplete]: [1]
[dev.pm.dyn_samplingrate]: [1]
[fmas.spkr_2ch]: [35,25]
[fmas.spkr_6ch]: [35,20,110]
[fmas.spkr_angles]: [10]
[fmas.spkr_sgain]: [0]
[gsm.current.phone-type]: [1]
[gsm.network.type]: [Unknown]
[gsm.operator.alpha]: []
[gsm.operator.iso-country]: []
[gsm.operator.isroaming]: [false]
[gsm.operator.numeric]: []
[gwm.mfi.addr]: [16]
[gwm.mfi.bus]: [/dev/i2c-0]
[hwservicemanager.ready]: [true]
[init.svc.QnxLogServerProxyClient]: [running]
[init.svc.adbd]: [stopped]
[init.svc.alarm-hal-1-0]: [running]
[init.svc.amfsservice]: [running]
[init.svc.animexitclient]: [stopped]
[init.svc.audioextserver]: [running]
[init.svc.audioserver]: [running]
[init.svc.avmservice]: [running]
[init.svc.bean_variant_server]: [running]
[init.svc.beanpki_init]: [stopped]
[init.svc.beansshost]: [running]
[init.svc.beantee_hal_service]: [running]
[init.svc.beanteed]: [running]
[init.svc.bootanim]: [stopped]
[init.svc.bosch-nfs-sh]: [stopped]
[init.svc.bosch-vp0-guard-sh]: [running]
[init.svc.broadcastradio-hal-2-0]: [running]
[init.svc.busybox-telnetd]: [running]
[init.svc.cameraserver]: [running]
[init.svc.com.android.car.procfsinspector]: [running]
[init.svc.crashdata-sh]: [stopped]
[init.svc.display-color-hal-1-0]: [running]
[init.svc.dlt_daemon]: [running]
[init.svc.drm]: [running]
[init.svc.ethcfg]: [stopped]
[init.svc.ethcfg_vt3]: [stopped]
[init.svc.fdbus-name-server]: [running]
[init.svc.gatekeeper-1-0]: [running]
[init.svc.gatekeeperd]: [running]
[init.svc.gnss_publish]: [running]
[init.svc.health-hal-2-0]: [running]
[init.svc.healthd]: [running]
[init.svc.hidl_memory]: [running]
[init.svc.hostapd]: [running]
[init.svc.hwservicemanager]: [running]
[init.svc.incidentd]: [running]
[init.svc.installd]: [running]
[init.svc.irsc_util]: [stopped]
[init.svc.keymaster-4-0]: [running]
[init.svc.keystore]: [running]
[init.svc.lmkd]: [running]
[init.svc.localepropset]: [stopped]
[init.svc.logd]: [running]
[init.svc.logd-reinit]: [stopped]
[init.svc.mdnsd]: [running]
[init.svc.media]: [running]
[init.svc.mediadrm]: [running]
[init.svc.mediaextractor]: [running]
[init.svc.mediametrics]: [running]
[init.svc.netd]: [running]
[init.svc.perf-hal-1-0]: [running]
[init.svc.qcarcam_hal]: [running]
[init.svc.qcom-c_core-sh]: [stopped]
[init.svc.qcom-c_main-sh]: [stopped]
[init.svc.qcom-post-boot]: [stopped]
[init.svc.qcom-sh]: [stopped]
[init.svc.qti-testscripts]: [stopped]
[init.svc.receiverbasesoftware-hal-1-0]: [running]
[init.svc.sbrserver]: [running]
[init.svc.servicemanager]: [running]
[init.svc.smartservice]: [running]
[init.svc.someipd-1-0@vlan2]: [running]
[init.svc.someipd-1-0@vlan3]: [running]
[init.svc.statsd]: [running]
[init.svc.storaged]: [running]
[init.svc.store_wifi_mac]: [stopped]
[init.svc.surfaceflinger]: [running]
[init.svc.systemlogserver]: [running]
[init.svc.tboxifctrl_up]: [stopped]
[init.svc.thermalservice]: [running]
[init.svc.tombstoned]: [running]
[init.svc.ubx-gnss]: [stopped]
[init.svc.udsd-1-0]: [running]
[init.svc.ueventd]: [running]
[init.svc.update_verifier_nonencrypted]: [stopped]
[init.svc.usbd]: [stopped]
[init.svc.variant_service]: [running]
[init.svc.vendor-diag-hal-1-0]: [running]
[init.svc.vendor-log-hal-1-0]: [running]
[init.svc.vendor-sensor-sh]: [stopped]
[init.svc.vendor.audio-hal-2-0]: [running]
[init.svc.vendor.bluetooth-1-0]: [running]
[init.svc.vendor.boot-hal-1-0]: [running]
[init.svc.vendor.bosch.lcm_controller]: [running]
[init.svc.vendor.bosch.vehicle-hal-2.0]: [running]
[init.svc.vendor.camera-provider-2-4]: [running]
[init.svc.vendor.cas-hal-1-0]: [running]
[init.svc.vendor.configstore-hal]: [running]
[init.svc.vendor.display-hal-2-0]: [running]
[init.svc.vendor.drm-clearkey-hal-1-1]: [running]
[init.svc.vendor.drm-hal-1-0]: [running]
[init.svc.vendor.hvdcp_opti]: [stopped]
[init.svc.vendor.hwcomposer-2-2]: [running]
[init.svc.vendor.ipacm]: [running]
[init.svc.vendor.ipacm-diag]: [running]
[init.svc.vendor.manifest-sku]: [stopped]
[init.svc.vendor.mdm_launcher]: [stopped]
[init.svc.vendor.media.omx]: [running]
[init.svc.vendor.memtrack-hal-1-0]: [running]
[init.svc.vendor.msm_irqbalance]: [running]
[init.svc.vendor.pd_mapper]: [running]
[init.svc.vendor.qcom-usb-sh]: [stopped]
[init.svc.vendor.qrtr-ns]: [running]
[init.svc.vendor.qseecomd]: [running]
[init.svc.vendor.qti.hardware.display.allocator]: [running]
[init.svc.vendor.rmt_storage]: [stopped]
[init.svc.vendor.sensors-hal-1-0]: [running]
[init.svc.vendor.ssr_setup]: [stopped]
[init.svc.vendor.thermal-engine]: [running]
[init.svc.vendor.thermal-hal-1-0]: [running]
[init.svc.vendor.ts.firewall-1-0]: [running]
[init.svc.vendor.ts.gnss-1-0]: [running]
[init.svc.vendor.ts.iap-hal-1-0]: [running]
[init.svc.vendor.usb-gadget-hal-1-0]: [running]
[init.svc.vendor.usb-hal-1-0]: [running]
[init.svc.vendor.usbext-hal-1-0]: [running]
[init.svc.vendor.wifi_hal_legacy]: [running]
[init.svc.vndservicemanager]: [running]
[init.svc.vold]: [running]
[init.svc.wificond]: [running]
[init.svc.wlan_multiko]: [stopped]
[init.svc.wpa_supplicant]: [running]
[init.svc.zygote]: [running]
[init.svc.zygote_secondary]: [running]
[keyguard.no_require_sim]: [true]
[log.tag.BroadcastRadio.manager]: [DEBUG]
[log.tag.BroadcastRadioDefault.service]: [DEBUG]
[log.tag.BroadcastRadioService.jni]: [DEBUG]
[log.tag.Em.RadioController]: [DEBUG]
[log.tag.Em.RadioService]: [DEBUG]
[log.tag.stats_log]: [I]
[media.aac_51_output_enabled]: [true]
[media.stagefright.enable-aac]: [true]
[media.stagefright.enable-fma2dp]: [true]
[media.stagefright.enable-http]: [true]
[media.stagefright.enable-player]: [true]
[media.stagefright.enable-qcp]: [true]
[media.stagefright.enable-scan]: [true]
[mm.enable.smoothstreaming]: [true]
[mmp.enable.3g2]: [true]
[net.bt.name]: [Android]
[net.dns1]: [192.168.1.1]
[net.dns2]: []
[net.hostname]: [HAVAL_1AFC]
[net.qtaguid_enabled]: [1]
[net.tcp.2g_init_rwnd]: [10]
[net.tcp.buffersize.default]: [4096,87380,524288,4096,16384,110208]
[net.tcp.buffersize.edge]: [4093,26280,35040,4096,16384,35040]
[net.tcp.buffersize.evdo]: [4094,87380,524288,4096,16384,262144]
[net.tcp.buffersize.gprs]: [4092,8760,11680,4096,8760,11680]
[net.tcp.buffersize.hsdpa]: [4094,87380,1220608,4096,16384,1220608]
[net.tcp.buffersize.hspa]: [4094,87380,1220608,4096,16384,1220608]
[net.tcp.buffersize.hspap]: [4094,87380,1220608,4096,16384,1220608]
[net.tcp.buffersize.hsupa]: [4094,87380,1220608,4096,16384,1220608]
[net.tcp.buffersize.lte]: [2097152,4194304,8388608,262144,524288,1048576]
[net.tcp.buffersize.umts]: [4094,87380,110208,4096,16384,110208]
[net.tcp.buffersize.wifi]: [524288,2097152,4194304,262144,524288,1048576]
[net.tcp.default_init_rwnd]: [60]
[persist.adb.tcp.port]: [5555]
[persist.audio.fluence.speaker]: [true]
[persist.audio.fluence.voicecall]: [true]
[persist.audio.fluence.voicecomm]: [true]
[persist.audio.fluence.voicerec]: [false]
[persist.autolink.adapter.version]: [V21.09.01_20221223-190411]
[persist.autolink.appverion.avm]: [V0.0]
[persist.autolink.wireless.carplay]: [1]
[persist.backup.ntpServer]: [0.pool.ntp.org]
[persist.bean.account.state]: [0]
[persist.bean.brand.id]: [1]
[persist.bean.car.mode1]: [B03G]
[persist.bean.car.mode2]: [0]
[persist.bean.card.status]: [0]
[persist.bean.configure.code]: [CC6470BK23CPHEV]
[persist.bean.country.code]: [17]
[persist.bean.dms]: []
[persist.bean.engine.type]: [4]
[persist.bean.factory_mode]: [1]
[persist.bean.fota.env.fingerprint]: [p_17_1_b03g_0]
[persist.bean.fota.log.pkg]: [/data/nfs/nfs_ota/log/fota_package/]
[persist.bean.fota.log.service]: [/data/user_de/0/com.beantechs.fotaService/files/logs]
[persist.bean.fota.rb.conf]: [/data/user_de/0/com.beantechs.fotaService/files/conf]
[persist.beantechs.androidauto.enable]: [1]
[persist.beantechs.carplay.enable]: [1]
[persist.beantechs.hvac.showing]: [0]
[persist.beantechs.pki.acttime]: [2022年11月19日 01:21:31]
[persist.beantechs.pki.errorcode]: [00000000]
[persist.beantechs.pki.stage]: [01]
[persist.beantechs.pki.tspflowstep]: [0x6f]
[persist.beantechs.pkishow.logtime]: [2024-08-23T01:48:18]
[persist.beantechs.vehicle.id]: [LGWFFbpXBnM7qzyVK6pNbrGxgbw==]
[persist.beantechs.vehicle.sn]: [3V6U9CAJAM2210100046]
[persist.beantechs.vehicle.vin]: [LGWFFUA58PH000048]
[persist.bluetooth.a2dp_offload.cap]: [sbc-aac-aptx-aptxhd-ldac]
[persist.bluetooth.a2dp_offload.disabled]: [false]
[persist.bluetooth.enablenewavrcp]: [false]
[persist.bt.clock_boottime_alarm]: [false]
[persist.car.lpm]: [true]
[persist.data.df.agg.dl_pkt]: [10]
[persist.data.df.agg.dl_size]: [4096]
[persist.data.df.dev_name]: [rmnet_usb0]
[persist.data.df.dl_mode]: [5]
[persist.data.df.iwlan_mux]: [9]
[persist.data.df.mux_count]: [8]
[persist.data.df.ul_mode]: [5]
[persist.data.wda.enable]: [true]
[persist.debug.coresight.config]: [stm-events]
[persist.debug.kill_oversized_process]: [1]
[persist.debug.pmem.trace]: [1]
[persist.debug.trace]: [0]
[persist.debug.wfd.enable]: [1]
[persist.demo.hdmirotationlock]: [false]
[persist.fuse_sdcard]: [true]
[persist.log.tag]: [WARN]
[persist.log.tag.A2dpMediaBrowserService]: [WARN]
[persist.log.tag.AudioHalHelper]: [WARN]
[persist.log.tag.AudioHalStreamInHAL]: [WARN]
[persist.log.tag.AudioHalStreamOutHAL]: [WARN]
[persist.log.tag.AvrcpControllerSM]: [WARN]
[persist.log.tag.AvrcpControllerService]: [WARN]
[persist.log.tag.BeanAdapterLogger]: [WARN]
[persist.log.tag.BeanNavigationBarFragment]: [WARN]
[persist.log.tag.BeanPlatformAdapter]: [WARN]
[persist.log.tag.BluetoothDevice]: [WARN]
[persist.log.tag.BoschVehicleHal]: [WARN]
[persist.log.tag.CAR.AM]: [WARN]
[persist.log.tag.CAR.HAL]: [WARN]
[persist.log.tag.CarPlay]: [WARN]
[persist.log.tag.CarPlayStack]: [WARN]
[persist.log.tag.CarTimeService]: [WARN]
[persist.log.tag.ClusterService.HandleMsgTools]: [WARN]
[persist.log.tag.CoreSystemServer]: [WARN]
[persist.log.tag.DPC_Native]: [WARN]
[persist.log.tag.DrivingAnalysisService]: [WARN]
[persist.log.tag.ExtMapJob]: [WARN]
[persist.log.tag.GnssLocationProvider]: [WARN]
[persist.log.tag.JobScheduler]: [WARN]
[persist.log.tag.NullTag]: [WARN]
[persist.log.tag.PropertyHalService]: [WARN]
[persist.log.tag.RBS.LibWrapper]: [WARN]
[persist.log.tag.RBSLibWrapper]: [WARN]
[persist.log.tag.TLOG]: [WARN]
[persist.log.tag.TLOGLOGS]: [WARN]
[persist.log.tag.TSPS_TSPermissionManagerService]: [WARN]
[persist.log.tag.UFUnilog]: [WARN]
[persist.log.tag.VehicleClient]: [WARN]
[persist.log.tag.YFLinkManager]: [WARN]
[persist.log.tag.accChangex]: [WARN]
[persist.log.tag.android.hardware.bluetooth@1.0-impl-cypress]: [WARN]
[persist.log.tag.bt_hwcfg]: [WARN]
[persist.log.tag.dvm_lock_sample]: [WARN]
[persist.log.tag.gyroChangex]: [WARN]
[persist.log.tag.mfichip]: [WARN]
[persist.log.tag.sensord]: [WARN]
[persist.log.tag.vSomeIP]: [WARN]
[persist.logd.size]: [10000000]
[persist.mm.enable.prefetch]: [true]
[persist.multiple.channel.recording]: [true]
[persist.netd.stable_secret]: [62d6:fc85:afe:be5f:aba4:b108:d373:53bd]
[persist.rild.nitz_long_ons_0]: []
[persist.rild.nitz_long_ons_1]: []
[persist.rild.nitz_long_ons_2]: []
[persist.rild.nitz_long_ons_3]: []
[persist.rild.nitz_plmn]: []
[persist.rild.nitz_short_ons_0]: []
[persist.rild.nitz_short_ons_1]: []
[persist.rild.nitz_short_ons_2]: []
[persist.rild.nitz_short_ons_3]: []
[persist.rmnet.data.enable]: [true]
[persist.service.bdroid.bdaddr]: [be:ef:be:ef:57:44]
[persist.sys.boot.reason]: [reboot,shell]
[persist.sys.dalvik.vm.lib.2]: [libart.so]
[persist.sys.disable_rescue]: [true]
[persist.sys.displayinset.top]: [0]
[persist.sys.force_sw_gles]: [1]
[persist.sys.locale]: [pt-BR]
[persist.sys.sf.color_saturation]: [1.0]
[persist.sys.strictmode.disable]: [true]
[persist.sys.timezone]: [America/Cayenne]
[persist.sys.usb.config]: [none]
[persist.sys.webview.vmsize]: [178110864]
[persist.sys.wfd.virtual]: [0]
[persist.timed.enable]: [true]
[persist.vendor.audio.calfile0]: [/vendor/etc/acdbdata/adsp_avs_config.acdb]
[persist.vendor.audio.calfile1]: [/vendor/etc/acdbdata/ADP/Bluetooth_cal.acdb]
[persist.vendor.audio.calfile2]: [/vendor/etc/acdbdata/ADP/Codec_cal.acdb]
[persist.vendor.audio.calfile3]: [/vendor/etc/acdbdata/ADP/General_cal.acdb]
[persist.vendor.audio.calfile4]: [/vendor/etc/acdbdata/ADP/Global_cal.acdb]
[persist.vendor.audio.calfile5]: [/vendor/etc/acdbdata/ADP/Handset_cal.acdb]
[persist.vendor.audio.calfile6]: [/vendor/etc/acdbdata/ADP/Hdmi_cal.acdb]
[persist.vendor.audio.calfile7]: [/vendor/etc/acdbdata/ADP/Headset_cal.acdb]
[persist.vendor.audio.calfile8]: [/vendor/etc/acdbdata/ADP/Speaker_cal.acdb]
[persist.vendor.audio.fluence.speaker]: [true]
[persist.vendor.audio.fluence.tmic.enabled]: [false]
[persist.vendor.audio.fluence.voicecall]: [true]
[persist.vendor.audio.fluence.voicerec]: [false]
[persist.vendor.audio.ras.enabled]: [false]
[persist.vendor.audio.voicecall.speaker.stereo]: [true]
[persist.vendor.bosch.cfg.major.ver]: [0]
[persist.vendor.bosch.cfg.minor.ver]: [27]
[persist.vendor.bosch.cfg.sync.completed]: [1]
[persist.vendor.bosch.cfg.sys.lang.usr.setting]: [8]
[persist.vendor.bosch.cfg.usb3.mount.domain]: [0]
[persist.vendor.bosch.smartservice.rtc]: [1]
[persist.vendor.bosch.usb2.mode]: [host]
[persist.vendor.bt.a2dp_offload_cap]: [sbc-aptx-aptxtws-aptxhd-aac-ldac]
[persist.vendor.btstack.enable.splita2dp]: [false]
[persist.vendor.cne.feature]: [1]
[persist.vendor.crash.cnt]: [8]
[persist.vendor.crash.detect]: [true]
[persist.vendor.data.mode]: [concurrent]
[persist.vendor.gwm.cfg.2nd.row.seat.centre.armrest]: [0]
[persist.vendor.gwm.cfg.2nd.row.seat.cooling.level.type]: [0]
[persist.vendor.gwm.cfg.2nd.row.seat.headrest.adjustment]: [1]
[persist.vendor.gwm.cfg.2nd.row.seat.heat.switch.type]: [0]
[persist.vendor.gwm.cfg.2nd.row.seat.welcome.function]: [0]
[persist.vendor.gwm.cfg.3rd.row.seat.armrest.dock.port]: [0]
[persist.vendor.gwm.cfg.3rd.row.seat.massage]: [0]
[persist.vendor.gwm.cfg.3rd.row.seat.ventilation]: [0]
[persist.vendor.gwm.cfg.a.c.comfortable.mode]: [1]
[persist.vendor.gwm.cfg.a.c.self.drying]: [0]
[persist.vendor.gwm.cfg.a.c.system]: [2]
[persist.vendor.gwm.cfg.a.c.turns.on.automatically]: [0]
[persist.vendor.gwm.cfg.ac.generator.properties]: [2]
[persist.vendor.gwm.cfg.ac.max.fast.cooling]: [0]
[persist.vendor.gwm.cfg.ac.natural.wind]: [0]
[persist.vendor.gwm.cfg.ac.uvc.sterilization.lamp]: [0]
[persist.vendor.gwm.cfg.acc.sensor.control.module]: [0]
[persist.vendor.gwm.cfg.active.access.system]: [0]
[persist.vendor.gwm.cfg.active.air.intake.grille]: [0]
[persist.vendor.gwm.cfg.active.heat.preservation.function.of.battery.pack]: [0]
[persist.vendor.gwm.cfg.active.noise.reduction.system]: [0]
[persist.vendor.gwm.cfg.adaptive.front.lighting.system]: [0]
[persist.vendor.gwm.cfg.aeb.junction.assist]: [1]
[persist.vendor.gwm.cfg.aeb.switch.type]: [1]
[persist.vendor.gwm.cfg.ai.interactive.light]: [0]
[persist.vendor.gwm.cfg.air.bag]: [7]
[persist.vendor.gwm.cfg.air.conditioner]: [4]
[persist.vendor.gwm.cfg.air.purifier]: [4]
[persist.vendor.gwm.cfg.air.quality.system]: [1]
[persist.vendor.gwm.cfg.air.suspension.auto.easy.access.mode]: [0]
[persist.vendor.gwm.cfg.air.suspension.foot.kick.loading.mode]: [0]
[persist.vendor.gwm.cfg.air.suspension.jack.mode]: [0]
[persist.vendor.gwm.cfg.air.suspension.trailer.mode]: [0]
[persist.vendor.gwm.cfg.ambient.light.control]: [0]
[persist.vendor.gwm.cfg.amplifier]: [1]
[persist.vendor.gwm.cfg.antenna]: [3]
[persist.vendor.gwm.cfg.audio.parsing.multi.color.rhythm.mood.lamp]: [0]
[persist.vendor.gwm.cfg.audio.video.system]: [13]
[persist.vendor.gwm.cfg.auto.door.lock]: [1]
[persist.vendor.gwm.cfg.auto.evasive.steering]: [0]
[persist.vendor.gwm.cfg.auto.light.system]: [1]
[persist.vendor.gwm.cfg.auto.parking.system]: [3]
[persist.vendor.gwm.cfg.auto.stop.at.roadside]: [0]
[persist.vendor.gwm.cfg.automatic.power.down.control]: [0]
[persist.vendor.gwm.cfg.auxiliary.console.central.lcd.screen]: [0]
[persist.vendor.gwm.cfg.auxiliary.fuel.tank]: [0]
[persist.vendor.gwm.cfg.avh]: [1]
[persist.vendor.gwm.cfg.avh.switch.type]: [1]
[persist.vendor.gwm.cfg.avm.camera.parameters]: [2]
[persist.vendor.gwm.cfg.avp.pixels]: [0]
[persist.vendor.gwm.cfg.barrel.instrument.type]: [0]
[persist.vendor.gwm.cfg.battery.sensor]: [1]
[persist.vendor.gwm.cfg.battery.temperature.keep.with.gun]: [3]
[persist.vendor.gwm.cfg.bean_data_md5]: [7F62E8A716A7863357F40E391CD71C7E]
]persist.vendor.gwm.cfg.bean_file_version]: [cfgVersion:E0480037
[persist.vendor.gwm.cfg.bean_modify_utc]: [1672314962]
[persist.vendor.gwm.cfg.bidirection.charging]: [0]
[persist.vendor.gwm.cfg.ble.account.login]: [0]
[persist.vendor.gwm.cfg.blocking.prompt.type]: [0]
[persist.vendor.gwm.cfg.bluetooth]: [1]
[persist.vendor.gwm.cfg.bluetooth.adapter]: [0]
[persist.vendor.gwm.cfg.body.domain.controller]: [0]
[persist.vendor.gwm.cfg.braking.energy.recovery]: [1]
[persist.vendor.gwm.cfg.braking.mode]: [0]
[persist.vendor.gwm.cfg.car.wash.mode]: [0]
[persist.vendor.gwm.cfg.care.mode]: [0]
[persist.vendor.gwm.cfg.cco.tcc.switch.type]: [0]
[persist.vendor.gwm.cfg.ccu]: [0]
[persist.vendor.gwm.cfg.center.control.sw.moudle]: [3]
[persist.vendor.gwm.cfg.central.electronic.module]: [0]
[persist.vendor.gwm.cfg.charger.opening.cover]: [1]
[persist.vendor.gwm.cfg.charger.opening.cover.electric.switch.type]: [1]
[persist.vendor.gwm.cfg.child.lock]: [1]
[persist.vendor.gwm.cfg.child.mode]: [0]
[persist.vendor.gwm.cfg.child.presence.detection]: [0]
[persist.vendor.gwm.cfg.close.to.lighting.function]: [0]
[persist.vendor.gwm.cfg.close.to.lighting.show.link.sound.effect.virtual.sw]: [0]
[persist.vendor.gwm.cfg.close.to.lighting.show.virtual.sw]: [0]
[persist.vendor.gwm.cfg.cluster]: [5]
[persist.vendor.gwm.cfg.cluster.time.display]: [1]
[persist.vendor.gwm.cfg.cluster.unit.system]: [0]
[persist.vendor.gwm.cfg.clutch.overheat.reminder.function]: [1]
[persist.vendor.gwm.cfg.co.pilot.airbag.switch]: [1]
[persist.vendor.gwm.cfg.combination.type.of.infotainment.system]: [4]
[persist.vendor.gwm.cfg.comfortable.stop]: [0]
[persist.vendor.gwm.cfg.console.dock.port]: [0]
[persist.vendor.gwm.cfg.cruise.control]: [9]
[persist.vendor.gwm.cfg.cruise.operation.mode]: [1]
[persist.vendor.gwm.cfg.crystal.console.panel]: [0]
[persist.vendor.gwm.cfg.crystal.panel.virtual.switch.link.wpc]: [0]
[persist.vendor.gwm.cfg.dab.broadcast]: [0]
[persist.vendor.gwm.cfg.damper]: [0]
[persist.vendor.gwm.cfg.danger.one.click.rescue]: [0]
[persist.vendor.gwm.cfg.deck]: [0]
[persist.vendor.gwm.cfg.deck.cover]: [0]
[persist.vendor.gwm.cfg.deck.lamp]: [0]
[persist.vendor.gwm.cfg.deck.rr.plate]: [0]
[persist.vendor.gwm.cfg.default.temperature.unit]: [0]
[persist.vendor.gwm.cfg.discharge.connecting.device]: [0]
[persist.vendor.gwm.cfg.dms.camera.parameters]: [5]
[persist.vendor.gwm.cfg.dms.type]: [1]
[persist.vendor.gwm.cfg.door.e.unlock]: [0]
[persist.vendor.gwm.cfg.door.module.type]: [1]
[persist.vendor.gwm.cfg.door.unlock.mode]: [1]
[persist.vendor.gwm.cfg.dr.open.warning]: [1]
[persist.vendor.gwm.cfg.drive.curtain]: [0]
[persist.vendor.gwm.cfg.drive.handle.type]: [0]
[persist.vendor.gwm.cfg.drive.type]: [0]
[persist.vendor.gwm.cfg.driver.belt]: [2]
[persist.vendor.gwm.cfg.driver.door.handle]: [4]
[persist.vendor.gwm.cfg.driver.headrest.speaker]: [0]
[persist.vendor.gwm.cfg.driver.seat]: [0]
[persist.vendor.gwm.cfg.driver.seat.cooling]: [1]
[persist.vendor.gwm.cfg.driver.seat.cushion.flank]: [0]
[persist.vendor.gwm.cfg.driver.seat.headrest.adjustment]: [1]
[persist.vendor.gwm.cfg.driver.seat.massage]: [0]
[persist.vendor.gwm.cfg.driver.seat.massage.pattern]: [0]
[persist.vendor.gwm.cfg.driver.seat.massage.strength.level]: [0]
[persist.vendor.gwm.cfg.driver.seat.rhythm.function]: [0]
[persist.vendor.gwm.cfg.driver.waist.supporter]: [2]
[persist.vendor.gwm.cfg.driver.window.operating]: [3]
[persist.vendor.gwm.cfg.driving.mode.2]: [0]
[persist.vendor.gwm.cfg.driving.mode.3]: [26]
[persist.vendor.gwm.cfg.driving.mode.master.control]: [1]
[persist.vendor.gwm.cfg.driving.mode.optional]: [9]
[persist.vendor.gwm.cfg.driving.mode.optional.vehicle.configuration.information]: [0]
[persist.vendor.gwm.cfg.driving.mode.signal.select]: [2]
[persist.vendor.gwm.cfg.drowsiness.warning.system]: [1]
[persist.vendor.gwm.cfg.dvr]: [0]
[persist.vendor.gwm.cfg.dvr.camera.parameters]: [0]
[persist.vendor.gwm.cfg.dynamic.steering.torque]: [1]
[persist.vendor.gwm.cfg.e.axle]: [0]
[persist.vendor.gwm.cfg.e.park]: [0]
[persist.vendor.gwm.cfg.electric.children.lock.virtual.sw]: [0]
[persist.vendor.gwm.cfg.electric.language]: [5]
[persist.vendor.gwm.cfg.electric.sound.reminder]: [1]
[persist.vendor.gwm.cfg.electrical.energy.management]: [1]
[persist.vendor.gwm.cfg.electromotor.position]: [6]
[persist.vendor.gwm.cfg.electronic.steering.column.lock]: [0]
[persist.vendor.gwm.cfg.electronic.toll.collection.etc]: [0]
[persist.vendor.gwm.cfg.emergency.call.system.e.call]: [3]
[persist.vendor.gwm.cfg.emergency.steering.support]: [0]
[persist.vendor.gwm.cfg.emission.level]: [11]
[persist.vendor.gwm.cfg.engine.control.unit]: [1]
[persist.vendor.gwm.cfg.engine.immobilizer]: [1]
[persist.vendor.gwm.cfg.engine.main.water.pump]: [1]
[persist.vendor.gwm.cfg.engine.oil.pressure.alarm.and.display]: [0]
[persist.vendor.gwm.cfg.engine.oil.temperature.display]: [0]
[persist.vendor.gwm.cfg.epb.switch.type]: [1]
[persist.vendor.gwm.cfg.epb.type]: [2]
[persist.vendor.gwm.cfg.esp.switch.type]: [1]
[persist.vendor.gwm.cfg.ess.system]: [1]
[persist.vendor.gwm.cfg.exclusive.business.mode]: [0]
[persist.vendor.gwm.cfg.first.row.air.mode.control.switch]: [0]
[persist.vendor.gwm.cfg.first.row.temperature.control.switch]: [0]
[persist.vendor.gwm.cfg.forward.collision.warning.auto.emergency.braking]: [5]
[persist.vendor.gwm.cfg.fr.windshield.heating.noozle]: [0]
[persist.vendor.gwm.cfg.fragrance.system]: [0]
[persist.vendor.gwm.cfg.front.air.outlet]: [0]
[persist.vendor.gwm.cfg.front.back.voice.call]: [0]
[persist.vendor.gwm.cfg.front.cross.warning.break]: [0]
[persist.vendor.gwm.cfg.front.headrest.neck.brace]: [0]
[persist.vendor.gwm.cfg.front.passen.seat.rhythm.function]: [0]
[persist.vendor.gwm.cfg.front.passenger.belt]: [2]
[persist.vendor.gwm.cfg.front.passenger.screen]: [0]
[persist.vendor.gwm.cfg.front.passenger.seat.headrest.adjustment]: [1]
[persist.vendor.gwm.cfg.front.passenger.seat.welcome.function]: [0]
[persist.vendor.gwm.cfg.front.radar.auto.turn.on]: [1]
[persist.vendor.gwm.cfg.front.sensor]: [4]
[persist.vendor.gwm.cfg.front.windshield.heating]: [0]
[persist.vendor.gwm.cfg.front.wiper.system]: [2]
[persist.vendor.gwm.cfg.frt.bumper]: [1]
[persist.vendor.gwm.cfg.frt.dead.angle.system]: [0]
[persist.vendor.gwm.cfg.frt.outer.sensor]: [1]
[persist.vendor.gwm.cfg.frt.seat.adj.switch.type]: [1]
[persist.vendor.gwm.cfg.frt.seat.belt]: [7]
[persist.vendor.gwm.cfg.frt.seat.cooling.frt.seat.massage]: [1]
[persist.vendor.gwm.cfg.frt.seat.cooling.level.type]: [1]
[persist.vendor.gwm.cfg.frt.seat.heat.switch.type]: [0]
[persist.vendor.gwm.cfg.frt.seat.heating.level.type]: [0]
[persist.vendor.gwm.cfg.frt.stabilizer]: [1]
[persist.vendor.gwm.cfg.fuel]: [4]
[persist.vendor.gwm.cfg.fuel.tank.system]: [3]
[persist.vendor.gwm.cfg.full.auto.integrated.parking.pixels]: [2]
[persist.vendor.gwm.cfg.game.center.function]: [0]
[persist.vendor.gwm.cfg.game.gear]: [1]
[persist.vendor.gwm.cfg.gesture.call]: [0]
[persist.vendor.gwm.cfg.gnss.module.type]: [0]
[persist.vendor.gwm.cfg.haptic.reminder.of.enhanced.assiet.systems]: [0]
[persist.vendor.gwm.cfg.haptic.reminder.of.lane.support.systems]: [1]
[persist.vendor.gwm.cfg.hdc.switch.type]: [1]
[persist.vendor.gwm.cfg.head.lamp.adjustment]: [1]
[persist.vendor.gwm.cfg.head.lamp.auto.off]: [1]
[persist.vendor.gwm.cfg.head.lamp.beam.system]: [0]
[persist.vendor.gwm.cfg.head.lamp.lighting]: [3]
[persist.vendor.gwm.cfg.head.up.display]: [1]
[persist.vendor.gwm.cfg.headlamp.control.function]: [0]
[persist.vendor.gwm.cfg.headlamp.virtual.sw]: [0]
[persist.vendor.gwm.cfg.high.low.auto.switching.beam.virtual.sw]: [0]
[persist.vendor.gwm.cfg.high.low.pressure.mode.for.fota]: [0]
[persist.vendor.gwm.cfg.highway.assist]: [0]
[persist.vendor.gwm.cfg.highway.pilot.hwp]: [0]
[persist.vendor.gwm.cfg.human.computer.interaction]: [0]
[persist.vendor.gwm.cfg.hut.1000base.ethernet.port]: [2]
[persist.vendor.gwm.cfg.hut.ethernet.port]: [2]
[persist.vendor.gwm.cfg.ibooster.config]: [2]
[persist.vendor.gwm.cfg.idc.l2]: [0]
[persist.vendor.gwm.cfg.idc.l3]: [0]
[persist.vendor.gwm.cfg.idle.stop.and.go]: [0]
[persist.vendor.gwm.cfg.iess.function]: [0]
[persist.vendor.gwm.cfg.indoor.automatic.demisting]: [1]
[persist.vendor.gwm.cfg.inst.refueling.port.orientation.display]: [1]
[persist.vendor.gwm.cfg.instrument.style]: [0]
[persist.vendor.gwm.cfg.integrated.brake.control.system]: [0]
[persist.vendor.gwm.cfg.integrated.child.seat]: [0]
[persist.vendor.gwm.cfg.intelligengt.driving.controller]: [0]
[persist.vendor.gwm.cfg.intelligent.curve.sw.type]: [1]
[persist.vendor.gwm.cfg.intelligent.front.camera]: [1]
[persist.vendor.gwm.cfg.intelligent.interactive.robot]: [0]
[persist.vendor.gwm.cfg.intelligent.network.service]: [1]
[persist.vendor.gwm.cfg.iss.light.show.switch]: [0]
[persist.vendor.gwm.cfg.lane.change.assist]: [1]
[persist.vendor.gwm.cfg.ldw.lka]: [8]
[persist.vendor.gwm.cfg.led.ultra.long.assisted.high.beam]: [0]
[persist.vendor.gwm.cfg.leg.supporter]: [0]
[persist.vendor.gwm.cfg.lighting.exhibition.hall.mode]: [0]
[persist.vendor.gwm.cfg.lighting.show.function]: [0]
[persist.vendor.gwm.cfg.limited.slip.differrential]: [0]
[persist.vendor.gwm.cfg.locking.light.show.virtual.sw]: [0]
[persist.vendor.gwm.cfg.low.beam.height.adj.virtual.sw]: [0]
[persist.vendor.gwm.cfg.low.speed.auto.emergency.brake.l.aeb]: [1]
[persist.vendor.gwm.cfg.meditation.mode]: [0]
[persist.vendor.gwm.cfg.memory.of.driving.mode]: [1]
[persist.vendor.gwm.cfg.mobile.bluetooth.key.system]: [0]
[persist.vendor.gwm.cfg.mobile.data.center.mdc]: [0]
[persist.vendor.gwm.cfg.mood.lamp]: [3]
[persist.vendor.gwm.cfg.mood.lamp.partition]: [0]
[persist.vendor.gwm.cfg.mp5.screen]: [2]
[persist.vendor.gwm.cfg.music.light.show]: [0]
[persist.vendor.gwm.cfg.navigation]: [1]
[persist.vendor.gwm.cfg.navigation.on.highwaypilot]: [0]
[persist.vendor.gwm.cfg.navigation.slowdown]: [0]
[persist.vendor.gwm.cfg.nfc.function]: [0]
[persist.vendor.gwm.cfg.night.vision.system]: [0]
[persist.vendor.gwm.cfg.none]: [0]
[persist.vendor.gwm.cfg.normal.tire.pressure]: [2]
[persist.vendor.gwm.cfg.off.road.cruise.control]: [0]
[persist.vendor.gwm.cfg.off.road.expert.mode]: [0]
[persist.vendor.gwm.cfg.off.road.information.display]: [0]
[persist.vendor.gwm.cfg.off.road.thermal.management.mode]: [0]
[persist.vendor.gwm.cfg.oil.level.display.and.alarm]: [0]
[persist.vendor.gwm.cfg.omniview.auto.turn.on.at.low.speed]: [0]
[persist.vendor.gwm.cfg.omniview.system]: [1]
[persist.vendor.gwm.cfg.omniview.system.vehicle.configuration.information]: [3]
[persist.vendor.gwm.cfg.oms.camera.parameters]: [0]
[persist.vendor.gwm.cfg.oms.type]: [0]
[persist.vendor.gwm.cfg.osrvm.adj.switch.type]: [1]
[persist.vendor.gwm.cfg.osrvm.fold.virtual.sw.control]: [0]
[persist.vendor.gwm.cfg.ouside.temperature.display]: [1]
[persist.vendor.gwm.cfg.outside.rr.view.mirror]: [3]
[persist.vendor.gwm.cfg.outside.voices]: [0]
[persist.vendor.gwm.cfg.parking.brake]: [2]
[persist.vendor.gwm.cfg.parking.lamp]: [0]
[persist.vendor.gwm.cfg.pas.cta]: [4]
[persist.vendor.gwm.cfg.pass.seat.memory.type]: [0]
[persist.vendor.gwm.cfg.pass.waist.supporter]: [0]
[persist.vendor.gwm.cfg.passenger.seat]: [2]
[persist.vendor.gwm.cfg.passenger.seat.cooling]: [1]
[persist.vendor.gwm.cfg.passenger.seat.massage]: [0]
[persist.vendor.gwm.cfg.passenger.seat.massage.pattern]: [0]
[persist.vendor.gwm.cfg.passenger.seat.massage.strength.level]: [0]
[persist.vendor.gwm.cfg.passenger.seat.memory.assistant]: [0]
[persist.vendor.gwm.cfg.passenger.window.operating]: [4]
[persist.vendor.gwm.cfg.pedal.control]: [1]
[persist.vendor.gwm.cfg.power.train.type]: [61]
[persist.vendor.gwm.cfg.product.name]: [1]
[persist.vendor.gwm.cfg.project.code]: [115]
[persist.vendor.gwm.cfg.pt.can.bus.type]: [1]
[persist.vendor.gwm.cfg.quick.inner.loop.mode]: [0]
[persist.vendor.gwm.cfg.quick.start]: [1]
[persist.vendor.gwm.cfg.radiator.grille]: [0]
[persist.vendor.gwm.cfg.rainy.and.snowy.day.mode]: [0]
[persist.vendor.gwm.cfg.rear.collision.warning]: [1]
[persist.vendor.gwm.cfg.rear.pas.sensor]: [4]
[persist.vendor.gwm.cfg.rear.trunk.spoiler]: [1]
[persist.vendor.gwm.cfg.rear.video]: [0]
[persist.vendor.gwm.cfg.rear.wheel.large.angle.steering]: [0]
[persist.vendor.gwm.cfg.rear.wheel.steering]: [0]
[persist.vendor.gwm.cfg.refeshing.mode]: [0]
[persist.vendor.gwm.cfg.regional]: [7]
[persist.vendor.gwm.cfg.remote.control]: [1]
[persist.vendor.gwm.cfg.remote.parking]: [0]
[persist.vendor.gwm.cfg.remote.reservation.charging]: [1]
[persist.vendor.gwm.cfg.remote.vehicle.environment.view]: [0]
[persist.vendor.gwm.cfg.reverse.video]: [0]
[persist.vendor.gwm.cfg.rr.1st.l.seat.adjustment]: [0]
[persist.vendor.gwm.cfg.rr.1st.r.seat.adjustment]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.adjustment]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.back.adjustment]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.cooling.rr.1st.seat.massage]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.fast.set]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.heating.level.type]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.leg.supporter]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.memory.function]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.one.click.reset]: [0]
[persist.vendor.gwm.cfg.rr.1st.seat.waist.supporter]: [0]
[persist.vendor.gwm.cfg.rr.1st.window.operating]: [4]
[persist.vendor.gwm.cfg.rr.2nd.seat.back.adjustment]: [0]
[persist.vendor.gwm.cfg.rr.2nd.seat.heating]: [0]
[persist.vendor.gwm.cfg.rr.2nd.seat.leg.supporter]: [0]
[persist.vendor.gwm.cfg.rr.a.c]: [0]
[persist.vendor.gwm.cfg.rr.bumper]: [1]
[persist.vendor.gwm.cfg.rr.door.opening]: [3]
[persist.vendor.gwm.cfg.rr.sliding.window]: [0]
[persist.vendor.gwm.cfg.rsca.protection.function]: [0]
[persist.vendor.gwm.cfg.rvc.camera.parameters]: [2]
[persist.vendor.gwm.cfg.sales.area]: [0]
[persist.vendor.gwm.cfg.seat.belt]: [2]
[persist.vendor.gwm.cfg.seat.control.module]: [0]
[persist.vendor.gwm.cfg.seat.cooling.auto.turn.on]: [0]
[persist.vendor.gwm.cfg.seat.heating]: [0]
[persist.vendor.gwm.cfg.seat.heating.auto.turn.on]: [0]
[persist.vendor.gwm.cfg.seat.massage.switch.type]: [0]
[persist.vendor.gwm.cfg.seat.memory.type]: [0]
[persist.vendor.gwm.cfg.second.left.seat.massage.pattern]: [0]
[persist.vendor.gwm.cfg.second.right.seat.massage.strength.level]: [0]
[persist.vendor.gwm.cfg.second.row.a.c.lock.control.switch]: [0]
[persist.vendor.gwm.cfg.second.row.a.c.on.off.virtual.sw]: [0]
[persist.vendor.gwm.cfg.second.row.air.mode.control.switch]: [0]
[persist.vendor.gwm.cfg.second.row.air.speed.control.switch]: [0]
[persist.vendor.gwm.cfg.second.row.seat.massage.switch.type]: [0]
[persist.vendor.gwm.cfg.second.row.temperature.control.switch]: [0]
[persist.vendor.gwm.cfg.second.row.voice.button]: [0]
[persist.vendor.gwm.cfg.secong.roght.seat.massage.pattern]: [0]
[persist.vendor.gwm.cfg.sentinel.mode]: [0]
[persist.vendor.gwm.cfg.service.brake]: [2]
[persist.vendor.gwm.cfg.shifted.unlock.key]: [0]
[persist.vendor.gwm.cfg.short.time.residence]: [0]
[persist.vendor.gwm.cfg.side.step]: [0]
[persist.vendor.gwm.cfg.smart.junction.box]: [1]
[persist.vendor.gwm.cfg.smart.start.stop.switch.memory.setting]: [0]
[persist.vendor.gwm.cfg.smoking.mode]: [0]
[persist.vendor.gwm.cfg.spare.tire.mtg]: [0]
[persist.vendor.gwm.cfg.speaker]: [4]
[persist.vendor.gwm.cfg.special.country.export]: [17]
[persist.vendor.gwm.cfg.speed.sensing.reverse]: [1]
[persist.vendor.gwm.cfg.speed.sensing.sunroof.switch]: [0]
[persist.vendor.gwm.cfg.speedometer]: [1]
[persist.vendor.gwm.cfg.sports.mode.lighting.prompt.s.repeater]: [0]
[persist.vendor.gwm.cfg.sreering.mode.of.expert]: [0]
[persist.vendor.gwm.cfg.starry.sky.ceiling]: [0]
[persist.vendor.gwm.cfg.starting.system]: [1]
[persist.vendor.gwm.cfg.stbs.ac.button]: [0]
[persist.vendor.gwm.cfg.steering.heating]: [0]
[persist.vendor.gwm.cfg.steering.mode]: [1]
[persist.vendor.gwm.cfg.steering.system]: [1]
[persist.vendor.gwm.cfg.steering.wheel.back.reminder]: [0]
[persist.vendor.gwm.cfg.steering.wheel.button]: [0]
[persist.vendor.gwm.cfg.steering.wheel.correction.assistance]: [0]
[persist.vendor.gwm.cfg.steering.wheel.heating.auto.turn.on]: [0]
[persist.vendor.gwm.cfg.strg.column]: [2]
[persist.vendor.gwm.cfg.sun.roof.controller]: [1]
[persist.vendor.gwm.cfg.sun.roof.shade.switch.type]: [1]
[persist.vendor.gwm.cfg.super.i.space]: [0]
[persist.vendor.gwm.cfg.super.i.space.ktv.mode]: [0]
[persist.vendor.gwm.cfg.super.lock]: [0]
[persist.vendor.gwm.cfg.suspension.mode.configuration.information]: [0]
[persist.vendor.gwm.cfg.suspension.spring.type]: [1]
[persist.vendor.gwm.cfg.sync.completed]: [1]
[persist.vendor.gwm.cfg.tab]: [0]
[persist.vendor.gwm.cfg.tab.switch.type]: [0]
[persist.vendor.gwm.cfg.tail.gate.switch.type]: [1]
[persist.vendor.gwm.cfg.tailgate.adj.virtual.sw]: [0]
[persist.vendor.gwm.cfg.telematics]: [1]
[persist.vendor.gwm.cfg.third.row.voice.button]: [0]
[persist.vendor.gwm.cfg.tpms]: [1]
[persist.vendor.gwm.cfg.traffic.light.and.stop.sign.control]: [0]
[persist.vendor.gwm.cfg.traffic.sign.warning]: [2]
[persist.vendor.gwm.cfg.trailer.sway.mitigation.function]: [0]
[persist.vendor.gwm.cfg.trailing.hook]: [0]
[persist.vendor.gwm.cfg.transfer.case]: [4]
[persist.vendor.gwm.cfg.transmission]: [19]
[persist.vendor.gwm.cfg.transmission.immobilizer]: [1]
[persist.vendor.gwm.cfg.trim.level]: [3]
[persist.vendor.gwm.cfg.type.of.booster.brake.pump]: [1]
[persist.vendor.gwm.cfg.ultrasonic.anti.theft.in.vehcle]: [0]
[persist.vendor.gwm.cfg.ultraviolet.germicidal.lamp]: [0]
[persist.vendor.gwm.cfg.unlock.light.show.virtual.sw]: [0]
[persist.vendor.gwm.cfg.unlocking.locking.prompt.sound]: [0]
[persist.vendor.gwm.cfg.up.down.hill]: [3]
[persist.vendor.gwm.cfg.vehicle.ota.mode.for.fota]: [0]
[persist.vendor.gwm.cfg.vehicle.to.load.discharge]: [0]
[persist.vendor.gwm.cfg.vehicle.to.vehicle.charge]: [0]
[persist.vendor.gwm.cfg.vehicle.to.x]: [0]
[persist.vendor.gwm.cfg.video.data.recorder]: [1]
[persist.vendor.gwm.cfg.virtual.sw.for.front.fog.lamp]: [0]
[persist.vendor.gwm.cfg.virtual.sw.for.rear.fog.lamp]: [0]
[persist.vendor.gwm.cfg.virtual.sw.for.strg.whl.handle.shift]: [0]
[persist.vendor.gwm.cfg.voice.facial.recognition]: [1]
[persist.vendor.gwm.cfg.voice.recognition]: [1]
[persist.vendor.gwm.cfg.vsg.type]: [2]
[persist.vendor.gwm.cfg.wade.mode]: [1]
[persist.vendor.gwm.cfg.wade.sw.type]: [2]
[persist.vendor.gwm.cfg.waist.supporter.switch.type]: [1]
[persist.vendor.gwm.cfg.warm.men.mode]: [0]
[persist.vendor.gwm.cfg.washing.liquid.level.alarm]: [0]
[persist.vendor.gwm.cfg.water.depth.detection]: [0]
[persist.vendor.gwm.cfg.water.temperature.display.of.instrument]: [0]
[persist.vendor.gwm.cfg.water.thermometer.display.parameters]: [1]
[persist.vendor.gwm.cfg.wheel.heat.switch.type]: [0]
[persist.vendor.gwm.cfg.window.short.lift.drop.function]: [0]
[persist.vendor.gwm.cfg.wiper.intermittent.level.virtual.sw]: [0]
[persist.vendor.gwm.cfg.wireless.power.charger]: [1]
[persist.vendor.gwm.cfg.wireless.power.transfer.system]: [0]
[persist.vendor.hvdcp_opti.version]: [3:0:0]
[persist.vendor.ims.disabled]: [1]
[persist.vendor.log.tag.androidkernal]: [INFO]
[persist.vendor.log.tag.app]: [INFO]
[persist.vendor.log.tag.audio]: [INFO]
[persist.vendor.log.tag.bsp]: [INFO]
[persist.vendor.log.tag.cluster]: [INFO]
[persist.vendor.log.tag.diag]: [INFO]
[persist.vendor.log.tag.errmem]: [INFO]
[persist.vendor.log.tag.esm]: [INFO]
[persist.vendor.log.tag.eth]: [INFO]
[persist.vendor.log.tag.inc]: [INFO]
[persist.vendor.log.tag.kernel]: [INFO]
[persist.vendor.log.tag.lifecyclemanagement]: [INFO]
[persist.vendor.log.tag.other]: [INFO]
[persist.vendor.log.tag.system]: [INFO]
[persist.vendor.log.tag.vehs]: [INFO]
[persist.vendor.log.tag.video]: [INFO]
[persist.vendor.qcomsysd.enabled]: [1]
[persist.vendor.radio.apm_sim_not_pwdn]: [1]
[persist.vendor.radio.atfwd.start]: [true]
[persist.vendor.radio.custom_ecc]: [1]
[persist.vendor.radio.rat_on]: [combine]
[persist.vendor.radio.sib16_support]: [1]
[persist.vendor.service.bdroid.sibs]: [false]
[persist.vendor.service.bt.a2dp.sink]: [true]
[persist.vendor.ssr.restart_level]: [wlan]
[persist.vendor.usb.config.extra]: [none]
[pm.dexopt.ab-ota]: [speed-profile]
[pm.dexopt.bg-dexopt]: [speed-profile]
[pm.dexopt.boot]: [verify]
[pm.dexopt.first-boot]: [quicken]
[pm.dexopt.inactive]: [verify]
[pm.dexopt.install]: [speed-profile]
[pm.dexopt.priv-apps-oob]: [false]
[pm.dexopt.priv-apps-oob-list]: [ALL]
[pm.dexopt.shared]: [speed]
[qcom.hw.aac.encoder]: [true]
[qemu.hw.mainkeys]: [0]
[ril.subscription.types]: [NV,RUIM]
[rild.libpath]: [/vendor/lib64/libril-qc-hal-qmi.so]
[ro.actionable_compatible_property.enabled]: [true]
[ro.adb.secure]: [1]
[ro.af.client_heap_size_kbyte]: [7168]
[ro.allow.mock.location]: [0]
[ro.audio.flinger_standbytime_ms]: [500]
[ro.baseband]: [unknown]
[ro.bean.gwm_osver_b01g1_0]: [S018A03XKN17001]
[ro.bean.gwm_osver_b01gind_0]: [12AQGBC147S0269]
[ro.bean.gwm_osver_b01gtha_0]: [12AQGBC147S0269]
[ro.bean.gwm_osver_b03g_0]: [S018A03XKN17001]
[ro.bean.gwm_osver_v510_0]: [12AQGBC147S0269]
[ro.bean.gwm_osver_v61_0]: [12AQGBC147S0269]
[ro.bean.gwm_osver_v71_0]: [12AQGBC147S0269]
[ro.bean.gwm_osver_v71phev_0]: [12AQGBC147S0269]
[ro.bean.ime.size]: [null]
[ro.bean.project.id]: [gbc147]
[ro.bean.project.name]: [BUX1.1_B01]
[ro.bean.variant_enable]: [1]
[ro.bean.watermark]: [0]
[ro.beantechs.appcfg_path]: [null]
[ro.bluetooth.a2dp_offload.supported]: [true]
[ro.bluetooth.emb_wp_mode]: [false]
[ro.bluetooth.wipower]: [false]
[ro.board.platform]: [msmnile]
[ro.boot.avb_version]: [1.1]
[ro.boot.bootdevice]: [/dev/disk/system_b]
[ro.boot.bootreason]: [reboot,shell]
[ro.boot.console]: [ttyAMA0]
[ro.boot.flash.locked]: [0]
[ro.boot.hardware]: [qcom]
[ro.boot.memcg]: [1]
[ro.boot.product.hardware.sku]: [362]
[ro.boot.selinux]: [permissive]
[ro.boot.serialno]: [1234567]
[ro.boot.usbcontroller]: [a600000.dwc3]
[ro.boot.vbmeta.avb_version]: [1.1]
[ro.boot.vbmeta.device]: [/dev/vdl]
[ro.boot.vbmeta.device_state]: [unlocked]
[ro.boot.vbmeta.digest]: [23b7568f43a1931e6ab32b68f91eb45b081ed6a508c3838e57f99058737a0b01]
[ro.boot.vbmeta.hash_alg]: [sha256]
[ro.boot.vbmeta.size]: [3264]
[ro.boot.verifiedbootstate]: [orange]
[ro.boot.veritymode]: [enforcing]
[ro.boot.wificountrycode]: [CN]
[ro.bootimage.build.date]: [Thu Dec 29 19:53:51 CST 2022]
[ro.bootimage.build.date.utc]: [1672314831]
[ro.bootimage.build.fingerprint]: [qti/gwm/gwm:9/PQ1A.190105.004/bean12291953:user/test-keys]
[ro.bootloader]: [unknown]
[ro.bootmode]: [unknown]
[ro.boottime.QnxLogServerProxyClient]: [2171349165]
[ro.boottime.alarm-hal-1-0]: [2204668801]
[ro.boottime.amfsservice]: [2523282863]
[ro.boottime.animexitclient]: [17434553794]
[ro.boottime.audioextserver]: [2207578957]
[ro.boottime.audioserver]: [2219157655]
[ro.boottime.avmservice]: [1448273176]
[ro.boottime.bean_variant_server]: [2155019270]
[ro.boottime.beanpki_init]: [2586485363]
[ro.boottime.beansshost]: [2530634165]
[ro.boottime.beantee_hal_service]: [2192614686]
[ro.boottime.beanteed]: [2531676613]
[ro.boottime.bootanim]: [4014017133]
[ro.boottime.bosch-nfs-sh]: [11209117130]
[ro.boottime.bosch-vp0-guard-sh]: [11211872651]
[ro.boottime.broadcastradio-hal-2-0]: [2515864842]
[ro.boottime.busybox-telnetd]: [2220415884]
[ro.boottime.cameraserver]: [2532881040]
[ro.boottime.com.android.car.procfsinspector]: [2221722655]
[ro.boottime.crashdata-sh]: [2589254634]
[ro.boottime.display-color-hal-1-0]: [2196709530]
[ro.boottime.dlt_daemon]: [1869393072]
[ro.boottime.drm]: [2534061561]
[ro.boottime.ethcfg]: [2508422134]
[ro.boottime.ethcfg_vt3]: [1420455051]
[ro.boottime.fdbus-name-server]: [1450346561]
[ro.boottime.gatekeeper-1-0]: [1453999895]
[ro.boottime.gatekeeperd]: [2591805155]
[ro.boottime.gnss_publish]: [2189295311]
[ro.boottime.health-hal-2-0]: [2177921249]
[ro.boottime.healthd]: [2169728645]
[ro.boottime.hidl_memory]: [2168657603]
[ro.boottime.hostapd]: [64691909349]
[ro.boottime.hwservicemanager]: [1438625364]
[ro.boottime.incidentd]: [2536619946]
[ro.boottime.init]: [819]
[ro.boottime.init.cold_boot_wait]: [75]
[ro.boottime.init.mount_all.default]: [44]
[ro.boottime.init.selinux]: [120]
[ro.boottime.installd]: [2538870571]
[ro.boottime.irsc_util]: [2213534426]
[ro.boottime.keymaster-4-0]: [1454851978]
[ro.boottime.keystore]: [2542902499]
[ro.boottime.lmkd]: [2222970572]
[ro.boottime.localepropset]: [2513533228]
[ro.boottime.logd]: [1437265416]
[ro.boottime.logd-reinit]: [1931186561]
[ro.boottime.mdnsd]: [2564174946]
[ro.boottime.media]: [2570808853]
[ro.boottime.mediadrm]: [2565287811]
[ro.boottime.mediaextractor]: [2566356874]
[ro.boottime.mediametrics]: [2568735936]
[ro.boottime.netd]: [1902582186]
[ro.boottime.perf-hal-1-0]: [2206626249]
[ro.boottime.qcarcam_hal]: [2199787655]
[ro.boottime.qcom-c_core-sh]: [2209385572]
[ro.boottime.qcom-c_main-sh]: [2519672655]
[ro.boottime.qcom-post-boot]: [10656227807]
[ro.boottime.qcom-sh]: [2587955519]
[ro.boottime.qti-testscripts]: [10657333432]
[ro.boottime.receiverbasesoftware-hal-1-0]: [2225379842]
[ro.boottime.sbrserver]: [2170653020]
[ro.boottime.servicemanager]: [1437973801]
[ro.boottime.smartservice]: [2190382915]
[ro.boottime.someipd-1-0@vlan2]: [1878831718]
[ro.boottime.someipd-1-0@vlan3]: [1879559582]
[ro.boottime.statsd]: [2581258696]
[ro.boottime.storaged]: [2582632915]
[ro.boottime.store_wifi_mac]: [11217304838]
[ro.boottime.surfaceflinger]: [2223790519]
[ro.boottime.systemlogserver]: [1881876405]
[ro.boottime.tboxifctrl_up]: [13574214421]
[ro.boottime.thermalservice]: [2224584582]
[ro.boottime.tombstoned]: [2593655311]
[ro.boottime.udsd-1-0]: [2191862082]
[ro.boottime.ueventd]: [1059308957]
[ro.boottime.update_verifier_nonencrypted]: [1882965988]
[ro.boottime.usbd]: [2595109217]
[ro.boottime.variant_service]: [1451367134]
[ro.boottime.vendor-diag-hal-1-0]: [2193412290]
[ro.boottime.vendor-log-hal-1-0]: [2195929269]
[ro.boottime.vendor-sensor-sh]: [2216450624]
[ro.boottime.vendor.audio-hal-2-0]: [2162643280]
[ro.boottime.vendor.bluetooth-1-0]: [2172274165]
[ro.boottime.vendor.boot-hal-1-0]: [1453123436]
[ro.boottime.vendor.bosch.lcm_controller]: [2195003072]
[ro.boottime.vendor.bosch.vehicle-hal-2.0]: [2514780728]
[ro.boottime.vendor.camera-provider-2-4]: [2173077811]
[ro.boottime.vendor.cas-hal-1-0]: [2173864947]
[ro.boottime.vendor.configstore-hal]: [2174609374]
[ro.boottime.vendor.display-hal-2-0]: [2194208801]
[ro.boottime.vendor.drm-clearkey-hal-1-1]: [2176369165]
[ro.boottime.vendor.drm-hal-1-0]: [2175537915]
[ro.boottime.vendor.hvdcp_opti]: [2529345936]
[ro.boottime.vendor.hwcomposer-2-2]: [2177155103]
[ro.boottime.vendor.ipacm]: [2807754061]
[ro.boottime.vendor.ipacm-diag]: [2793347446]
[ro.boottime.vendor.manifest-sku]: [1210144530]
[ro.boottime.vendor.mdm_launcher]: [2525649634]
[ro.boottime.vendor.media.omx]: [2585054738]
[ro.boottime.vendor.memtrack-hal-1-0]: [2178846874]
[ro.boottime.vendor.msm_irqbalance]: [2757249582]
[ro.boottime.vendor.pd_mapper]: [2218343644]
[ro.boottime.vendor.qcom-usb-sh]: [2217455311]
[ro.boottime.vendor.qrtr-ns]: [2211148332]
[ro.boottime.vendor.qseecomd]: [1447127134]
[ro.boottime.vendor.qti.hardware.display.allocator]: [2205714894]
[ro.boottime.vendor.rmt_storage]: [2215007707]
[ro.boottime.vendor.sensors-hal-1-0]: [2179670988]
[ro.boottime.vendor.ssr_setup]: [2506156092]
[ro.boottime.vendor.thermal-engine]: [2521141249]
[ro.boottime.vendor.thermal-hal-1-0]: [2182729165]
[ro.boottime.vendor.ts.firewall-1-0]: [2517425103]
[ro.boottime.vendor.ts.gnss-1-0]: [2518524217]
[ro.boottime.vendor.ts.iap-hal-1-0]: [2208479426]
[ro.boottime.vendor.usb-gadget-hal-1-0]: [2197455207]
[ro.boottime.vendor.usb-hal-1-0]: [2198224947]
[ro.boottime.vendor.usbext-hal-1-0]: [2199029217]
[ro.boottime.vendor.wifi_hal_legacy]: [2183849009]
[ro.boottime.vndservicemanager]: [1439266093]
[ro.boottime.vold]: [1455972759]
[ro.boottime.wificond]: [2583829634]
[ro.boottime.wlan_multiko]: [2510644686]
[ro.boottime.wpa_supplicant]: [11122708953]
[ro.boottime.zygote]: [1903430728]
[ro.boottime.zygote_secondary]: [1904305103]
[ro.bosch.dbc.ver]: [B30-006-014DB01  CAN DataBase for SC-CAN_V6.0]
[ro.bosch.hw.board.info.fw.ver]: [N900251.1]
[ro.bosch.hw.board.info.hw.id]: [CAJAM-773]
[ro.bosch.hw.board.info.hw.ver]: [5.1.0.23]
[ro.bosch.hw.board.info.name]: [BOARD_INFO]
[ro.bosch.hw.board.info.node.addr]: [CAJAM-773]
[ro.bosch.hw.board.info.pcb.level.partnumber]: [8638905015]
[ro.bosch.hw.board.info.pn]: [7901104XKN31A]
[ro.bosch.hw.board.info.sn]: [3V6U9CAJAM2210100046]
[ro.bosch.veh.mfr]: [Great Wall Motors]
[ro.bosch.veh.vin]: [LGWFFUA58PH000048]
[ro.build.ab_update]: [true]
[ro.build.characteristics]: [nosdcard]
[ro.build.date]: [Thu Dec 29 19:53:51 CST 2022]
[ro.build.date.utc]: [1672314831]
[ro.build.description]: [gwm-user 9 PQ1A.190105.004 eng.bean.20221229.195411 test-keys]
[ro.build.display.id]: [PQ1A.190105.004 test-keys]
[ro.build.fingerprint]: [qti/gwm/gwm:9/PQ1A.190105.004/bean12291953:user/test-keys]
[ro.build.flavor]: [gwm-user]
[ro.build.forcecleansize]: [512]
[ro.build.host]: [d0688404f8cc]
[ro.build.id]: [PQ1A.190105.004]
[ro.build.product]: [gwm]
[ro.build.system_root_image]: [true]
[ro.build.tags]: [test-keys]
[ro.build.type]: [user]
[ro.build.user]: [bean]
[ro.build.version.all_codenames]: [REL]
[ro.build.version.base_os]: []
[ro.build.version.codename]: [REL]
[ro.build.version.incremental]: [eng.bean.20221229.195411]
[ro.build.version.min_supported_target_sdk]: [17]
[ro.build.version.preview_sdk]: [0]
[ro.build.version.release]: [9]
[ro.build.version.sdk]: [28]
[ro.build.version.security_patch]: [2020-02-05]
[ro.build.warningdatasize]: [1024]
[ro.carrier]: [unknown]
[ro.com.android.dataroaming]: [true]
[ro.config.alarm_alert]: [Alarm_Classic.ogg]
[ro.config.notification_sound]: [pixiedust.ogg]
[ro.config.ringtone]: [Ring_Synth_04.ogg]
[ro.crypto.state]: [encrypted]
[ro.crypto.type]: [file]
[ro.dalvik.vm.native.bridge]: [0]
[ro.debuggable]: [0]
[ro.device_owner]: [false]
[ro.frp.pst]: [/dev/block/bootdevice/by-name/frp]
[ro.hardware]: [qcom]
[ro.hardware.camera]: [ais]
[ro.hardware.keystore_desede]: [true]
[ro.hardware.nfc_nci]: [nqx.default]
[ro.hardware.type]: [automotive]
[ro.hwui.drop_shadow_cache_size]: [6]
[ro.hwui.gradient_cache_size]: [1]
[ro.hwui.layer_cache_size]: [48]
[ro.hwui.path_cache_size]: [32]
[ro.hwui.r_buffer_cache_size]: [8]
[ro.hwui.text_large_cache_height]: [1024]
[ro.hwui.text_large_cache_width]: [2048]
[ro.hwui.text_small_cache_height]: [1024]
[ro.hwui.text_small_cache_width]: [1024]
[ro.hwui.texture_cache_flushrate]: [0.4]
[ro.hwui.texture_cache_size]: [72]
[ro.kernel.qemu.gles]: [0]
[ro.leading.car.model]: [gbc147]
[ro.lmk.enable_adaptive_lmk]: [true]
[ro.lmk.enhance_batch_kill]: [true]
[ro.lmk.kill_heaviest_task]: [true]
[ro.lmk.kill_timeout_ms]: [15]
[ro.lmk.use_minfree_levels]: [false]
[ro.lmk.vmpressure_file_min]: [80640]
[ro.lockscreen.disable.default]: [true]
[ro.logd.auditd.dmesg]: [false]
[ro.logd.auditd.events]: [false]
[ro.logd.size.stats]: [64K]
[ro.nfc.port]: [I2C]
[ro.oem_unlock_supported]: [1]
[ro.opengles.version]: [196610]
[ro.persistent_properties.ready]: [true]
[ro.platform.env.type]: [P]
[ro.product.board]: [msmnile]
[ro.product.brand]: [qti]
[ro.product.cpu.abi]: [arm64-v8a]
[ro.product.cpu.abilist]: [arm64-v8a,armeabi-v7a,armeabi]
[ro.product.cpu.abilist32]: [armeabi-v7a,armeabi]
[ro.product.cpu.abilist64]: [arm64-v8a]
[ro.product.device]: [gwm]
[ro.product.locale]: [en-US]
[ro.product.manufacturer]: [QUALCOMM]
[ro.product.model]: [msmnile_gvmq for arm64]
[ro.product.name]: [gwm]
[ro.product.vendor.brand]: [qti]
[ro.product.vendor.device]: [gwm]
[ro.product.vendor.manufacturer]: [QUALCOMM]
[ro.product.vendor.model]: [msmnile_gvmq for arm64]
[ro.product.vendor.name]: [gwm]
[ro.property_service.version]: [2]
[ro.qc.sdk.audio.fluencetype]: [none]
[ro.qc.sdk.audio.ssr]: [false]
[ro.revision]: [0]
[ro.runtime.firstboot]: [1724388495520]
[ro.secure]: [1]
[ro.serialno]: [1234567]
[ro.sf.lcd_density]: [160]
[ro.software.version]: [1.1.00.1BP_GBC147S0269]
[ro.telephony.call_ring.multiple]: [false]
[ro.treble.enabled]: [true]
[ro.vendor.alarm_boot]: [false]
[ro.vendor.audio.sdk.fluencetype]: [none]
[ro.vendor.audio.sdk.ssr]: [false]
[ro.vendor.build.date]: [Thu Dec 29 19:53:51 CST 2022]
[ro.vendor.build.date.utc]: [1672314831]
[ro.vendor.build.fingerprint]: [qti/gwm/gwm:9/PQ1A.190105.004/bean12291953:user/test-keys]
[ro.vendor.build.security_patch]: [2018-08-05]
[ro.vendor.display.cabl]: [2]
[ro.vendor.extension_library]: [libqti-perfd-client.so]
[ro.vendor.product.cpu.abilist]: [arm64-v8a,armeabi-v7a,armeabi]
[ro.vendor.product.cpu.abilist32]: [armeabi-v7a,armeabi]
[ro.vendor.product.cpu.abilist64]: [arm64-v8a]
[ro.vendor.qti.config.zram]: [true]
[ro.vendor.qti.sys.fw.bg_apps_limit]: [60]
[ro.vendor.ril.mbn_copy_completed]: [1]
[ro.vendor.scroll.preobtain.enable]: [true]
[ro.vendor.use_data_netmgrd]: [true]
[ro.vndk.version]: [28]
[ro.wifi.channels]: []
[ro.zygote]: [zygote64_32]
[security.perf_harden]: [1]
[selinux.restorecon_recursive]: [/data/misc_ce/0]
[service.bootanim.exit]: [1]
[service.ivi.bootanim.exit]: [1]
[service.sf.present_timestamp]: [1]
[storage.cpu.load.memory]: [1]
[sys.autolink.adapter.start.count]: [1]
[sys.bean.bootAnimation_complete]: [1]
[sys.bean.brightness_bar_enable]: [0]
[sys.bean.datatrack.enable]: [0]
[sys.bean.guide_complete]: [0]
[sys.bean.guide_complete_time]: [26145]
[sys.bean.guide_state]: [1]
[sys.bean.journey.id]: [2d496316a419277e64f165882188fc2A]
[sys.bean.remote_upgrade_state]: [0]
[sys.bean.volume_bar_enable]: [0]
[sys.boot.reason]: [reboot,shell]
[sys.boot_completed]: [1]
[sys.com.ts.car.power.controller.core.standby_mode]: [0]
[sys.logbootcomplete]: [1]
[sys.oem_unlock_allowed]: [0]
[sys.qca1530]: [detect]
[sys.retaildemo.enabled]: [0]
[sys.sysctl.extra_free_kbytes]: [81000]
[sys.sysctl.tcp_def_init_rwnd]: [60]
[sys.usb.config]: [none]
[sys.usb.configfs]: [1]
[sys.usb.controller]: [a600000.dwc3]
[sys.usb.ffs.ready]: [0]
[sys.usb.mtp.device_type]: [2]
[sys.usb.state]: [none]
[sys.user.0.ce_available]: [true]
[sys.vendor.shutdown.waittime]: [500]
[sys.wifi.driver.status]: [ok]
[sys.wifi.driver.version]: [Dongle Host Driver, version 100.10.5.12 (r726086)]
[sys.wifi.firmware.version]: [Firmware: wl0: Sep 13 2022 23:41:22 version 13.35.239.17 (fd01cfa CY) FWID 01-5eef4f42]
[sys.wifi.hardware.version]: [Chip: 4355 Rev d Pkg 2]
[sys.wifi.mac]: [28:0f:eb:5e:1a:fd]
[sys.wifi.softap_interface_name]: [wlan2]
[sys.wifitracing.started]: [1]
[telephony.lteOnCdmaDevice]: [1]
[tunnel.audio.encode]: [true]
[use.voice.path.for.pcm.voip]: [true]
[vendor.audio.adm.buffering.ms]: [2]
[vendor.audio.dolby.ds2.enabled]: [false]
[vendor.audio.dolby.ds2.hardbypass]: [false]
[vendor.audio.enable.mirrorlink]: [false]
[vendor.audio.flac.sw.decoder.24bit]: [true]
[vendor.audio.hal.maj.version]: [3]
[vendor.audio.hal.output.suspend.supported]: [false]
[vendor.audio.hw.aac.encoder]: [false]
[vendor.audio.noisy.broadcast.delay]: [600]
[vendor.audio.offload.buffer.size.kb]: [32]
[vendor.audio.offload.gapless.enabled]: [true]
[vendor.audio.offload.multiaac.enable]: [true]
[vendor.audio.offload.multiple.enabled]: [false]
[vendor.audio.offload.passthrough]: [false]
[vendor.audio.offload.pstimeout.secs]: [3]
[vendor.audio.offload.track.enable]: [true]
[vendor.audio.parser.ip.buffer.size]: [262144]
[vendor.audio.safx.pbe.enabled]: [true]
[vendor.audio.tunnel.encode]: [false]
[vendor.audio.use.hw.ape.decoder]: [true]
[vendor.audio.use.hw.wma.decoder]: [true]
[vendor.audio.use.sw.alac.decoder]: [true]
[vendor.audio.use.sw.ape.decoder]: [true]
[vendor.audio_hal.in_period_size]: [144]
[vendor.audio_hal.period_multiplier]: [3]
[vendor.audio_hal.period_size]: [192]
[vendor.audioext.first.start]: [1]
[vendor.audioext.hal.adapter]: [libaudioexthaladapter.so]
[vendor.audioext.set.device.volume]: [1]
[vendor.camera.aux.packagelist]: [org.codeaurora.snapcam]
[vendor.display.builtin_mirroring]: [true]
[vendor.display.comp_mask]: [0]
[vendor.display.dataspace_saturation_matrix]: [1.0,0.0,0.0,0.0,1.0,0.0,0.0,0.0,1.0]
[vendor.display.disable_decimation]: [1]
[vendor.display.disable_excl_rect]: [0]
[vendor.display.disable_hw_recovery_dump]: [1]
[vendor.display.disable_inline_rotator]: [1]
[vendor.display.disable_scaler]: [0]
[vendor.display.enable_default_color_mode]: [1]
[vendor.display.enable_null_display]: [0]
[vendor.display.enable_optimize_refresh]: [1]
[vendor.display.lcd_density]: [160]
[vendor.firewall.halservice]: [true]
[vendor.gralloc.disable_ubwc]: [0]
[vendor.gwm.audio.init.state]: [done]
[vendor.iop.enable_uxe]: [1]
[vendor.mm.enable.qcom_parser]: [63963135]
[vendor.perf.gestureflingboost.enable]: [true]
[vendor.perf.iop_v3.enable]: [true]
[vendor.post_boot.parsed]: [1]
[vendor.power.pasr.enabled]: [true]
[vendor.qcom.bluetooth.soc]: [hastings]
[vendor.sys.listeners.registered]: [true]
[vendor.tbox.connected]: [true]
[vendor.tswlan.carplay_over_wireless]: [true]
[vendor.usb.controller]: [a600000.dwc3]
[vendor.usb.dpl.inst.name]: [dpl]
[vendor.usb.rmnet.func.name]: [gsi]
[vendor.usb.rmnet.inst.name]: [rmnet]
[vendor.usb.rndis.func.name]: [gsi]
[vendor.usb.rps_mask]: [0]
[vendor.voice.path.for.pcm.voip]: [true]
[vendor.wifi.apband]: [1]
[vold.has_adoptable]: [1]
[vold.has_quota]: [1]
[vold.has_reserved]: [1]
[vold.post_fs_data_done]: [1]
[wifi.direct.interface]: [p2p-dev-wlan0]
[wifi.interface]: [wlan0]
[wlan.driver.status]: [ok]

```

ifconfig
```
:/mnt/vendor/persist # ifconfig
vlan11    Link encap:Ethernet  HWaddr 02:47:57:4d:00:99
          inet addr:172.16.11.99  Bcast:0.0.0.0  Mask:255.255.255.0 
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:71 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:0 TX bytes:13490 

vlan2     Link encap:Ethernet  HWaddr 02:47:57:4d:00:99
          inet addr:172.16.2.99  Bcast:0.0.0.0  Mask:255.255.255.0 
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:48285 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:11080 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:18149808 TX bytes:1830087 

dummy0    Link encap:Ethernet  HWaddr 7a:c5:ce:36:12:af
          inet6 addr: fe80::78c5:ceff:fe36:12af/64 Scope: Link
          UP BROADCAST RUNNING NOARP  MTU:1500  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:72 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:0 TX bytes:16406 

vlan4     Link encap:Ethernet  HWaddr 02:47:57:4d:00:99
          inet addr:172.16.4.99  Bcast:0.0.0.0  Mask:255.255.255.0 
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:71 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:0 TX bytes:13467 

vlan12    Link encap:Ethernet  HWaddr 02:47:57:4d:00:99
          inet addr:172.16.12.99  Bcast:0.0.0.0  Mask:255.255.255.0 
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:8909 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:71 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:748356 TX bytes:13490 

wlan0     Link encap:Ethernet  HWaddr 28:0f:eb:5e:1a:fd
          inet addr:192.168.1.197  Bcast:192.168.1.255  Mask:255.255.255.0 
          inet6 addr: fe80::2a0f:ebff:fe5e:1afd/64 Scope: Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:45197 errors:0 dropped:77 overruns:0 frame:0 
          TX packets:10571 errors:0 dropped:7 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:14189810 TX bytes:1709499 

wlan2     Link encap:Ethernet  HWaddr 2a:0f:eb:5e:5a:fd
          inet addr:192.168.33.128  Bcast:192.168.33.255  Mask:255.255.255.0 
          inet6 addr: fe80::280f:ebff:fe5e:5afd/64 Scope: Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:66553 errors:0 dropped:123 overruns:0 frame:0 
          TX packets:30337 errors:0 dropped:28 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:67548114 TX bytes:2394902 

vlan3     Link encap:Ethernet  HWaddr 02:47:57:4d:00:99
          inet addr:172.16.3.99  Bcast:0.0.0.0  Mask:255.255.255.0 
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:23156 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:8973 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:1766748 TX bytes:885783 

vt3       Link encap:Ethernet  HWaddr aa:aa:aa:aa:aa:b3  Driver virtio_net
          inet addr:192.168.118.1  Bcast:0.0.0.0  Mask:255.255.255.0 
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:682412 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:718413 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:93357335 TX bytes:41480022 

eth0      Link encap:Ethernet  HWaddr 02:47:57:4d:00:99  Driver virtio_net
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:80919 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:21016 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:22352075 TX bytes:2987636 

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0 
          inet6 addr: ::1/128 Scope: Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:1361840 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:1361840 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:458002802 TX bytes:458002802 

vlan13    Link encap:Ethernet  HWaddr 02:47:57:4d:00:99
          inet addr:172.16.13.99  Bcast:172.16.13.255  Mask:255.255.255.0 
          inet6 addr: fe80::7d83:81a1:463c:7821/64 Scope: Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:506 errors:0 dropped:0 overruns:0 frame:0 
          TX packets:751 errors:0 dropped:0 overruns:0 carrier:0 
          collisions:0 txqueuelen:1000 
          RX bytes:228101 TX bytes:147445 


```


netstat

```
:/mnt/vendor/persist # busybox netstat
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       
tcp        0      0 192.168.118.1:34206     192.168.118.2:65516     ESTABLISHED 
tcp        0      0 192.168.118.1:45635     192.168.118.2:65465     ESTABLISHED 
tcp        0      0 192.168.118.1:35466     192.168.118.2:65529     ESTABLISHED 
tcp        0      0 127.0.0.1:32044         127.0.0.1:64730         ESTABLISHED 
tcp        0      0 192.168.118.1:35388     192.168.118.2:65517     ESTABLISHED 
tcp        0      1 192.168.1.25:59186      34.120.195.249:443      FIN_WAIT1   
tcp        0      0 127.0.0.1:40988         127.0.0.1:22531         ESTABLISHED 
tcp        0      0 192.168.118.1:35200     192.168.118.2:65515     ESTABLISHED 
tcp        0      0 192.168.118.1:46206     192.168.118.2:65534     ESTABLISHED 
tcp       25      0 127.0.0.1:1234          127.0.0.1:41868         ESTABLISHED 
tcp        0      1 192.168.1.25:44260      35.190.43.134:443       FIN_WAIT1   
tcp        0      0 127.0.0.1:33942         127.0.0.1:22530         ESTABLISHED 
tcp        0      0 192.168.118.1:34202     192.168.118.2:65516     ESTABLISHED 
tcp        0      0 192.168.118.1:48652     192.168.118.2:65477     ESTABLISHED 
tcp        0      0 192.168.118.1:65184     192.168.118.2:65481     ESTABLISHED 
tcp        0      0 192.168.118.1:44120     192.168.118.2:65478     ESTABLISHED 
tcp        0      0 127.0.0.1:53480         127.0.0.1:22539         ESTABLISHED 
tcp        0      1 192.168.1.25:41216      13.36.185.156:443       LAST_ACK    
tcp        0      0 192.168.118.1:43806     192.168.118.2:60000     ESTABLISHED 
tcp        0      0 192.168.118.1:63900     192.168.118.2:65495     ESTABLISHED 
tcp        0      0 127.0.0.1:64768         127.0.0.1:22532         ESTABLISHED 
tcp        0      0 192.168.118.1:34590     192.168.118.2:65515     ESTABLISHED 
tcp        0      0 127.0.0.1:33974         127.0.0.1:22530         ESTABLISHED 
tcp        0      0 127.0.0.1:22531         127.0.0.1:40988         ESTABLISHED 
tcp        0      0 192.168.118.1:60001     192.168.118.2:65468     ESTABLISHED 
tcp        0      0 127.0.0.1:32098         127.0.0.1:52428         ESTABLISHED 
tcp        0      0 127.0.0.1:64730         127.0.0.1:32044         ESTABLISHED 
tcp        0      0 127.0.0.1:32046         127.0.0.1:37816         ESTABLISHED 
tcp        0      0 192.168.118.1:38078     192.168.118.2:65518     ESTABLISHED 
tcp        0      0 127.0.0.1:32042         127.0.0.1:41090         ESTABLISHED 
tcp        0      0 127.0.0.1:22529         127.0.0.1:64308         ESTABLISHED 
tcp        0      1 192.168.1.25:54676      172.67.36.125:443       FIN_WAIT1   
tcp        0      0 127.0.0.1:41090         127.0.0.1:32042         ESTABLISHED 
tcp        0      0 127.0.0.1:52428         127.0.0.1:32098         ESTABLISHED 
tcp        0      0 192.168.118.1:49966     192.168.118.2:65496     ESTABLISHED 
tcp        0      0 127.0.0.1:64308         127.0.0.1:22529         ESTABLISHED 
tcp        0      0 192.168.118.1:32981     192.168.118.2:65467     ESTABLISHED 
tcp        0      1 192.168.1.25:41234      13.36.185.156:443       LAST_ACK    
tcp        0   2670 192.168.1.197:9090      192.168.1.27:59072      ESTABLISHED 
tcp        0      0 192.168.118.1:58190     192.168.118.2:65490     ESTABLISHED 
tcp        0      0 192.168.118.1:37728     192.168.118.2:65515     ESTABLISHED 
tcp        0      0 192.168.1.197:9090      192.168.1.27:58804      ESTABLISHED 
tcp        0      0 127.0.0.1:33940         127.0.0.1:22530         ESTABLISHED 
tcp        0      0 192.168.118.1:39000     192.168.118.2:65523     ESTABLISHED 
tcp        0      1 192.168.1.25:45466      151.101.108.157:443     FIN_WAIT1   
tcp        0      0 192.168.1.197:42572     162.14.21.56:853        TIME_WAIT   
tcp        0      1 192.168.1.25:44258      35.190.43.134:443       FIN_WAIT1   
tcp        0      0 172.16.2.99:55001       172.16.2.97:55000       ESTABLISHED 
tcp        0      0 192.168.118.1:62248     192.168.118.2:65489     ESTABLISHED 
tcp        0      0 192.168.118.1:37089     192.168.118.2:65466     ESTABLISHED 
tcp        0      0 192.168.118.1:51626     192.168.118.2:65479     ESTABLISHED 
tcp        0      0 192.168.118.1:59146     192.168.118.2:60001     ESTABLISHED 
tcp        0      0 192.168.118.1:37738     192.168.118.2:65515     ESTABLISHED 
tcp        0      0 127.0.0.1:37816         127.0.0.1:32046         ESTABLISHED 
tcp        0      0 127.0.0.1:22532         127.0.0.1:64768         ESTABLISHED 
tcp        0      0 192.168.118.1:37742     192.168.118.2:65515     ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:22530  ::ffff:127.0.0.1:33974  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:41868  ::ffff:127.0.0.1:1234   ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:22559  ::ffff:127.0.0.1:45606  ESTABLISHED 
tcp        0    504 ::ffff:192.168.1.25:45942 ::ffff:119.8.84.203:443 LAST_ACK    
tcp        0      0 ::ffff:127.0.0.1:22559  ::ffff:127.0.0.1:51714  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:22530  ::ffff:127.0.0.1:33940  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:51714  ::ffff:127.0.0.1:22559  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:22539  ::ffff:127.0.0.1:53480  ESTABLISHED 
tcp        0    515 ::ffff:192.168.1.25:45940 ::ffff:119.8.84.203:443 LAST_ACK    
tcp        0      0 ::ffff:127.0.0.1:22559  ::ffff:127.0.0.1:45632  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:45632  ::ffff:127.0.0.1:22559  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:22530  ::ffff:127.0.0.1:33942  ESTABLISHED 
tcp        0      0 ::ffff:127.0.0.1:45606  ::ffff:127.0.0.1:22559  ESTABLISHED 
udp     2816      0 192.168.1.197:68        192.168.1.1:67          ESTABLISHED 
udp        0      0 127.0.0.1:38363         127.0.0.1:38363         ESTABLISHED 
udp        0      0 127.0.0.1:38389         127.0.0.1:30000         ESTABLISHED 
udp        0      0 172.16.3.99:55001       172.16.3.97:55000       ESTABLISHED 
udp        0      0 172.16.2.99:55001       172.16.2.97:55000       ESTABLISHED 
Active UNIX domain sockets (w/o servers)
Proto RefCnt Flags       Type       State         I-Node Path
unix  176    [ ]         DGRAM                     12377 /dev/socket/logdw
unix  2      [ ]         DGRAM                     29820 /dev/socket/wpa_wlan0
unix  2      [ ]         DGRAM                     55757 /data/vendor/wifi/hostapd/ctrl/wlan2
unix  2      [ ]         DGRAM                     29540 /data/vendor/wifi/wpa/sockets/wlan0
unix  4      [ ]         DGRAM                     16366 /dev/socket/statsdw
unix  2      [ ]         DGRAM                     14576 /dev/socket/ipacm_log_file
unix  3      [ ]         STREAM     CONNECTED      38813 
unix  3      [ ]         SEQPACKET  CONNECTED      76292 
unix  3      [ ]         SEQPACKET  CONNECTED      53461 
unix  3      [ ]         STREAM     CONNECTED      26064 /dev/socket/zygote
unix  2      [ ]         DGRAM                     24078 
unix  2      [ ]         DGRAM                     19865 
unix  2      [ ]         DGRAM                     16248 
unix  3      [ ]         SEQPACKET  CONNECTED      75877 
unix  3      [ ]         SEQPACKET  CONNECTED      50079 
unix  2      [ ]         DGRAM                     43057 
unix  3      [ ]         STREAM     CONNECTED      23593 
unix  2      [ ]         DGRAM                     12923 
unix  3      [ ]         SEQPACKET  CONNECTED      61376 
unix  2      [ ]         DGRAM                     15217 
unix  3      [ ]         SEQPACKET  CONNECTED      31418 
unix  2      [ ]         DGRAM                     10907 
unix  3      [ ]         STREAM     CONNECTED      11959 
unix  3      [ ]         STREAM     CONNECTED       9208 
unix  3      [ ]         SEQPACKET  CONNECTED      46198 
unix  3      [ ]         STREAM     CONNECTED      40520 
unix  3      [ ]         SEQPACKET  CONNECTED      62515 
unix  3      [ ]         STREAM     CONNECTED      47648 
unix  3      [ ]         STREAM     CONNECTED      24570 
unix  2      [ ]         DGRAM                     28429 
unix  2      [ ]         DGRAM                     17178 
unix  2      [ ]         DGRAM                     53015 
unix  3      [ ]         SEQPACKET  CONNECTED      46419 
unix  2      [ ]         DGRAM                     41179 
unix  3      [ ]         STREAM     CONNECTED      12908 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      46401 
unix  3      [ ]         STREAM     CONNECTED      45305 
unix  3      [ ]         STREAM     CONNECTED      14400 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      76154 
unix  3      [ ]         SEQPACKET  CONNECTED      50076 
unix  2      [ ]         DGRAM                     14095 
unix  3      [ ]         STREAM     CONNECTED      14401 @/data/misc/fdbus/fdb-ns
unix  2      [ ]         DGRAM                     42782 
unix  2      [ ]         DGRAM                     26839 
unix  3      [ ]         STREAM     CONNECTED      26073 /dev/socket/sbrserver
unix  2      [ ]         DGRAM                     17123 
unix  2      [ ]         DGRAM                     12264 
unix  3      [ ]         STREAM     CONNECTED      11958 
unix  3      [ ]         STREAM     CONNECTED      24571 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         STREAM     CONNECTED      40906 /dev/socket/mdnsd
unix  3      [ ]         SEQPACKET  CONNECTED      46350 
unix  2      [ ]         DGRAM                     13148 
unix  3      [ ]         SEQPACKET  CONNECTED      46533 
unix  2      [ ]         DGRAM                     14778 
unix  2      [ ]         DGRAM                     15447 
unix  3      [ ]         SEQPACKET  CONNECTED      76141 
unix  3      [ ]         SEQPACKET  CONNECTED      50139 
unix  2      [ ]         DGRAM                     12858 
unix  3      [ ]         SEQPACKET  CONNECTED      51601 
unix  2      [ ]         DGRAM                     24569 
unix  2      [ ]         DGRAM                     20939 
unix  2      [ ]         DGRAM                     18945 
unix  3      [ ]         STREAM     CONNECTED      17189 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      29360 
unix  3      [ ]         SEQPACKET  CONNECTED      21258 
unix  3      [ ]         STREAM     CONNECTED      40905 
unix  3      [ ]         SEQPACKET  CONNECTED      43658 
unix  3      [ ]         STREAM     CONNECTED      31189 
unix  3      [ ]         STREAM     CONNECTED      17507 
unix  2      [ ]         DGRAM                     26469 
unix  2      [ ]         DGRAM                     10312 
unix  3      [ ]         STREAM     CONNECTED      40908 
unix  3      [ ]         STREAM     CONNECTED      38884 
unix  2      [ ]         DGRAM                     24481 
unix  2      [ ]         DGRAM                     17238 
unix  3      [ ]         SEQPACKET  CONNECTED      26439 
unix  3      [ ]         STREAM     CONNECTED      16164 
unix  3      [ ]         SEQPACKET  CONNECTED      56118 
unix  3      [ ]         SEQPACKET  CONNECTED      29370 
unix  3      [ ]         STREAM     CONNECTED      28820 
unix  2      [ ]         DGRAM                     28368 
unix  2      [ ]         DGRAM                     44306 
unix  3      [ ]         SEQPACKET  CONNECTED      45465 
unix  3      [ ]         STREAM     CONNECTED      19555 
unix  2      [ ]         DGRAM                     20756 
unix  2      [ ]         DGRAM                     10886 
unix  3      [ ]         SEQPACKET  CONNECTED      40497 
unix  3      [ ]         SEQPACKET  CONNECTED      29788 
unix  2      [ ]         DGRAM                     12095 
unix  2      [ ]         DGRAM                     17511 
unix  3      [ ]         SEQPACKET  CONNECTED      76286 
unix  3      [ ]         SEQPACKET  CONNECTED      51421 
unix  3      [ ]         SEQPACKET  CONNECTED      29356 
unix  2      [ ]         DGRAM                     41341 
unix  3      [ ]         SEQPACKET  CONNECTED      76152 
unix  3      [ ]         SEQPACKET  CONNECTED      61377 
unix  3      [ ]         SEQPACKET  CONNECTED      50077 
unix  2      [ ]         DGRAM                     16398 
unix  3      [ ]         SEQPACKET  CONNECTED      46352 
unix  3      [ ]         STREAM     CONNECTED      13814 
unix  3      [ ]         STREAM     CONNECTED      40529 
unix  3      [ ]         SEQPACKET  CONNECTED      45299 
unix  3      [ ]         SEQPACKET  CONNECTED      26438 
unix  2      [ ]         DGRAM                     16267 
unix  3      [ ]         SEQPACKET  CONNECTED      75839 
unix  3      [ ]         SEQPACKET  CONNECTED      50085 
unix  2      [ ]         DGRAM                     14035 
unix  2      [ ]         DGRAM                     15276 
unix  2      [ ]         DGRAM                     20832 
unix  3      [ ]         SEQPACKET  CONNECTED      24103 
unix  2      [ ]         DGRAM                     17117 
unix  3      [ ]         SEQPACKET  CONNECTED      76338 
unix  3      [ ]         SEQPACKET  CONNECTED      53462 
unix  3      [ ]         SEQPACKET  CONNECTED      53087 
unix  3      [ ]         SEQPACKET  CONNECTED      54678 
unix  3      [ ]         STREAM     CONNECTED      40881 
unix  3      [ ]         STREAM     CONNECTED      38897 /data/misc/someip/172.16.3.99/vlan3-1346
unix  2      [ ]         DGRAM                     26543 
unix  2      [ ]         DGRAM                     18125 
unix  3      [ ]         STREAM     CONNECTED      44162 
unix  3      [ ]         SEQPACKET  CONNECTED      76143 
unix  3      [ ]         SEQPACKET  CONNECTED      24101 
unix  3      [ ]         SEQPACKET  CONNECTED      53465 
unix  3      [ ]         SEQPACKET  CONNECTED      26665 
unix  2      [ ]         DGRAM                     12499 
unix  3      [ ]         STREAM     CONNECTED      23589 
unix  2      [ ]         DGRAM                     24180 
unix  2      [ ]         DGRAM                     17100 
unix  3      [ ]         STREAM     CONNECTED      28821 @com.android.internal.os.WebViewZygoteInit/702b46cc-4218-454a-b3a6-6536987d4ae7
unix  3      [ ]         SEQPACKET  CONNECTED      53384 
unix  3      [ ]         STREAM     CONNECTED      28522 
unix  2      [ ]         DGRAM                     16213 
unix  2      [ ]         DGRAM                     91002 
unix  3      [ ]         SEQPACKET  CONNECTED      57374 
unix  3      [ ]         SEQPACKET  CONNECTED      45466 
unix  3      [ ]         SEQPACKET  CONNECTED      46367 
unix  3      [ ]         STREAM     CONNECTED      40530 @/data/misc/fdbus/fdb-ns
unix  2      [ ]         DGRAM                     41300 
unix  3      [ ]         STREAM     CONNECTED      38903 /data/misc/someip/172.16.2.99/vlan2-1351
unix  3      [ ]         SEQPACKET  CONNECTED      20963 
unix  3      [ ]         SEQPACKET  CONNECTED      11969 
unix  3      [ ]         SEQPACKET  CONNECTED      26638 
unix  2      [ ]         DGRAM                     26973 
unix  2      [ ]         DGRAM                     23183 
unix  3      [ ]         SEQPACKET  CONNECTED      75881 
unix  3      [ ]         SEQPACKET  CONNECTED      76299 
unix  2      [ ]         DGRAM                     41007 
unix  2      [ ]         DGRAM                     16169 
unix  2      [ ]         DGRAM                     14216 
unix  2      [ ]         DGRAM                     12710 
unix  3      [ ]         SEQPACKET  CONNECTED      46141 
unix  3      [ ]         SEQPACKET  CONNECTED      29766 
unix  3      [ ]         SEQPACKET  CONNECTED      24094 
unix  3      [ ]         STREAM     CONNECTED      20892 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         STREAM     CONNECTED      15898 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         STREAM     CONNECTED      43174 
unix  3      [ ]         SEQPACKET  CONNECTED      26637 
unix  2      [ ]         DGRAM                     13004 
unix  3      [ ]         SEQPACKET  CONNECTED      76344 
unix  3      [ ]         SEQPACKET  CONNECTED      24079 
unix  3      [ ]         SEQPACKET  CONNECTED      29352 
unix  2      [ ]         DGRAM                     19368 
unix  2      [ ]         DGRAM                    352314 
unix  3      [ ]         STREAM     CONNECTED      13817 /data/misc/someip/172.16.2.99/vlan2-1343
unix  2      [ ]         DGRAM                     20602 
unix  2      [ ]         DGRAM                     45710 
unix  3      [ ]         SEQPACKET  CONNECTED      56114 
unix  2      [ ]         DGRAM                     10945 
unix  3      [ ]         SEQPACKET  CONNECTED      24095 
unix  3      [ ]         STREAM     CONNECTED      16165 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      46199 
unix  2      [ ]         DGRAM                     14172 
unix  3      [ ]         SEQPACKET  CONNECTED      29350 
unix  3      [ ]         SEQPACKET  CONNECTED      21259 
unix  3      [ ]         SEQPACKET  CONNECTED      56478 
unix  3      [ ]         STREAM     CONNECTED      26063 
unix  2      [ ]         DGRAM                     17494 
unix  3      [ ]         SEQPACKET  CONNECTED      76337 
unix  2      [ ]         DGRAM                     48430 
unix  3      [ ]         STREAM     CONNECTED      17167 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      45297 
unix  3      [ ]         SEQPACKET  CONNECTED      76284 
unix  3      [ ]         STREAM     CONNECTED      38894 
unix  3      [ ]         STREAM     CONNECTED      26066 /dev/socket/zygote_secondary
unix  3      [ ]         SEQPACKET  CONNECTED      46353 
unix  3      [ ]         SEQPACKET  CONNECTED      26666 
unix  2      [ ]         STREAM     CONNECTED     154585 
unix  3      [ ]         SEQPACKET  CONNECTED      29357 
unix  3      [ ]         STREAM     CONNECTED      15897 
unix  3      [ ]         STREAM     CONNECTED      17166 
unix  3      [ ]         SEQPACKET  CONNECTED      46360 
unix  2      [ ]         DGRAM                     14052 
unix  3      [ ]         STREAM     CONNECTED      38885 /data/misc/someip/172.16.2.99/vlan2-1345
unix  3      [ ]         STREAM     CONNECTED      38881 
unix  3      [ ]         SEQPACKET  CONNECTED      29787 
unix  3      [ ]         SEQPACKET  CONNECTED      56113 
unix  2      [ ]         DGRAM                     17374 
unix  3      [ ]         SEQPACKET  CONNECTED      76305 
unix  2      [ ]         DGRAM                     44324 
unix  2      [ ]         DGRAM                     41119 
unix  3      [ ]         STREAM     CONNECTED      31187 /data/misc/someip/172.16.2.99/vlan2-0
unix  3      [ ]         SEQPACKET  CONNECTED      29789 
unix  3      [ ]         SEQPACKET  CONNECTED      11970 
unix  3      [ ]         SEQPACKET  CONNECTED      51422 
unix  3      [ ]         SEQPACKET  CONNECTED      46351 
unix  2      [ ]         DGRAM                     13737 
unix  2      [ ]         DGRAM                     10674 
unix  3      [ ]         SEQPACKET  CONNECTED      27475 
unix  2      [ ]         DGRAM                     16251 
unix  3      [ ]         SEQPACKET  CONNECTED      86765 
unix  2      [ ]         DGRAM                     24374 
unix  3      [ ]         SEQPACKET  CONNECTED      45298 
unix  2      [ ]         DGRAM                     14269 
unix  2      [ ]         DGRAM                     15347 
unix  2      [ ]         DGRAM                     12803 
unix  3      [ ]         SEQPACKET  CONNECTED      76283 
unix  3      [ ]         STREAM     CONNECTED      23592 
unix  3      [ ]         SEQPACKET  CONNECTED      48287 
unix  3      [ ]         STREAM     CONNECTED      31198 
unix  3      [ ]         SEQPACKET  CONNECTED      26436 
unix  3      [ ]         STREAM     CONNECTED      20891 
unix  3      [ ]         SEQPACKET  CONNECTED      11971 
unix  2      [ ]         DGRAM                     55177 
unix  3      [ ]         STREAM     CONNECTED      30013 
unix  2      [ ]         DGRAM                     11252 
unix  3      [ ]         SEQPACKET  CONNECTED      21261 
unix  2      [ ]         DGRAM                     16192 
unix  3      [ ]         SEQPACKET  CONNECTED      46361 
unix  3      [ ]         STREAM     CONNECTED      23591 
unix  2      [ ]         DGRAM                     12477 
unix  3      [ ]         STREAM     CONNECTED      38888 /data/misc/someip/172.16.2.99/vlan2-0
unix  3      [ ]         SEQPACKET  CONNECTED      46402 
unix  3      [ ]         STREAM     CONNECTED      40521 
unix  3      [ ]         SEQPACKET  CONNECTED      76293 
unix  3      [ ]         SEQPACKET  CONNECTED      54940 
unix  3      [ ]         STREAM     CONNECTED      38812 
unix  2      [ ]         DGRAM                     53214 
unix  2      [ ]         DGRAM                     24641 
unix  3      [ ]         STREAM     CONNECTED      16193 
unix  3      [ ]         SEQPACKET  CONNECTED      16471 /dev/socket/logdr
unix  3      [ ]         SEQPACKET  CONNECTED      75838 
unix  2      [ ]         DGRAM                     55753 
unix  3      [ ]         SEQPACKET  CONNECTED      53466 
unix  2      [ ]         DGRAM                     12492 
unix  2      [ ]         DGRAM                     44243 
unix  2      [ ]         DGRAM                     23091 
unix  2      [ ]         STREAM     CONNECTED     165394 
unix  3      [ ]         STREAM     CONNECTED      10660 /data/misc/someip/172.16.2.99/vlan2-0
unix  2      [ ]         DGRAM                     20899 
unix  3      [ ]         STREAM     CONNECTED      40882 
unix  3      [ ]         STREAM     CONNECTED      38901 /data/misc/someip/172.16.2.99/vlan2-134f
unix  3      [ ]         STREAM     CONNECTED      26065 
unix  3      [ ]         SEQPACKET  CONNECTED      46140 
unix  2      [ ]         DGRAM                     18276 
unix  3      [ ]         STREAM     CONNECTED      28448 
unix  2      [ ]         DGRAM                     17169 
unix  2      [ ]         DGRAM                     41939 
unix  2      [ ]         DGRAM                     45610 
unix  2      [ ]         DGRAM                     20823 
unix  2      [ ]         DGRAM                     44270 
unix  3      [ ]         STREAM     CONNECTED      23588 
unix  3      [ ]         SEQPACKET  CONNECTED      76285 
unix  3      [ ]         SEQPACKET  CONNECTED      50086 
unix  2      [ ]         DGRAM                     15109 
unix  3      [ ]         STREAM     CONNECTED      30012 
unix  3      [ ]         STREAM     CONNECTED      31197 
unix  2      [ ]         DGRAM                     26128 
unix  3      [ ]         STREAM     CONNECTED      18691 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      76144 
unix  3      [ ]         STREAM     CONNECTED      12503 
unix  3      [ ]         SEQPACKET  CONNECTED      54939 
unix  2      [ ]         DGRAM                     26802 
unix  2      [ ]         DGRAM                     19486 
unix  2      [ ]         DGRAM                     18775 
unix  3      [ ]         STREAM     CONNECTED      40333 
unix  3      [ ]         SEQPACKET  CONNECTED      24097 
unix  3      [ ]         STREAM     CONNECTED      40501 
unix  3      [ ]         STREAM     CONNECTED      45238 
unix  3      [ ]         STREAM     CONNECTED      46206 
unix  3      [ ]         STREAM     CONNECTED      18704 @/data/misc/fdbus/fdb-ns
unix  2      [ ]         DGRAM                     11078 
unix  2      [ ]         DGRAM                     13086 
unix  3      [ ]         STREAM     CONNECTED      16269 
unix  3      [ ]         SEQPACKET  CONNECTED      76151 
unix  2      [ ]         DGRAM                     12919 
unix  2      [ ]         DGRAM                     14399 
unix  3      [ ]         SEQPACKET  CONNECTED      40334 
unix  2      [ ]         DGRAM                     24398 
unix  3      [ ]         SEQPACKET  CONNECTED      62514 
unix  2      [ ]         DGRAM                     45756 
unix  2      [ ]         DGRAM                     41427 
unix  2      [ ]         DGRAM                     21004 
unix  2      [ ]         DGRAM                     26784 
unix  2      [ ]         DGRAM                     15896 
unix  3      [ ]         SEQPACKET  CONNECTED      76306 
unix  2      [ ]         DGRAM                     28253 
unix  3      [ ]         SEQPACKET  CONNECTED      24096 
unix  2      [ ]         DGRAM                     14114 
unix  3      [ ]         SEQPACKET  CONNECTED      29351 
unix  2      [ ]         DGRAM                     12539 
unix  2      [ ]         DGRAM                     41989 
unix  2      [ ]         DGRAM                     40984 
unix  3      [ ]         SEQPACKET  CONNECTED      46398 
unix  3      [ ]         SEQPACKET  CONNECTED      76336 
unix  3      [ ]         SEQPACKET  CONNECTED      57373 
unix  3      [ ]         SEQPACKET  CONNECTED      50140 
unix  2      [ ]         DGRAM                     24458 
unix  2      [ ]         DGRAM                     17399 
unix  3      [ ]         SEQPACKET  CONNECTED      26663 
unix  3      [ ]         STREAM     CONNECTED      23587 
unix  2      [ ]         DGRAM                     15521 
unix  3      [ ]         SEQPACKET  CONNECTED      75874 
unix  2      [ ]         DGRAM                     43392 
unix  2      [ ]         DGRAM                     12886 
unix  3      [ ]         STREAM     CONNECTED      38895 /data/misc/someip/172.16.2.99/vlan2-0
unix  3      [ ]         SEQPACKET  CONNECTED      43659 
unix  3      [ ]         STREAM     CONNECTED      43175 
unix  3      [ ]         STREAM     CONNECTED      44163 
unix  2      [ ]         DGRAM                     15240 
unix  3      [ ]         SEQPACKET  CONNECTED      27355 
unix  3      [ ]         SEQPACKET  CONNECTED      76148 
unix  3      [ ]         SEQPACKET  CONNECTED      57368 
unix  3      [ ]         SEQPACKET  CONNECTED      40335 
unix  3      [ ]         SEQPACKET  CONNECTED      14777 /dev/socket/lmkd
unix  2      [ ]         DGRAM                     20050 
unix  2      [ ]         DGRAM                     18759 
unix  2      [ ]         DGRAM                     12216 
unix  3      [ ]         SEQPACKET  CONNECTED      46399 
unix  2      [ ]         DGRAM                     23187 
unix  3      [ ]         STREAM     CONNECTED      15837 
unix  2      [ ]         DGRAM                      9209 
unix  3      [ ]         SEQPACKET  CONNECTED      75875 
unix  3      [ ]         SEQPACKET  CONNECTED      46534 
unix  2      [ ]         DGRAM                     44135 
unix  2      [ ]         DGRAM                     12979 
unix  3      [ ]         SEQPACKET  CONNECTED      76298 
unix  3      [ ]         STREAM     CONNECTED      28449 @/data/misc/fdbus/fdb-ns
unix  2      [ ]         DGRAM                     17187 
unix  3      [ ]         SEQPACKET  CONNECTED      45467 
unix  2      [ ]         DGRAM                     41506 
unix  3      [ ]         SEQPACKET  CONNECTED      21260 
unix  3      [ ]         STREAM     CONNECTED      23585 
unix  2      [ ]         DGRAM                     19641 
unix  3      [ ]         SEQPACKET  CONNECTED      31417 
unix  3      [ ]         SEQPACKET  CONNECTED      29790 
unix  3      [ ]         SEQPACKET  CONNECTED      46397 
unix  3      [ ]         STREAM     CONNECTED      40506 
unix  3      [ ]         SEQPACKET  CONNECTED      30056 
unix  3      [ ]         STREAM     CONNECTED      31199 
unix  2      [ ]         DGRAM                     13731 
unix  3      [ ]         SEQPACKET  CONNECTED      56117 
unix  3      [ ]         SEQPACKET  CONNECTED      11972 
unix  2      [ ]         DGRAM                    351285 
unix  3      [ ]         STREAM     CONNECTED      26080 
unix  2      [ ]         DGRAM                     20945 
unix  2      [ ]         DGRAM                     24274 
unix  3      [ ]         SEQPACKET  CONNECTED      16457 
unix  3      [ ]         STREAM     CONNECTED      23590 
unix  2      [ ]         DGRAM                     20077 
unix  2      [ ]         DGRAM                     13080 
unix  2      [ ]         DGRAM                     16237 
unix  3      [ ]         SEQPACKET  CONNECTED      53385 
unix  3      [ ]         STREAM     CONNECTED      47649 @/data/misc/fdbus/fdb-ns
unix  2      [ ]         DGRAM                     14241 
unix  3      [ ]         SEQPACKET  CONNECTED      29369 
unix  2      [ ]         DGRAM                     12801 
unix  3      [ ]         SEQPACKET  CONNECTED      46142 
unix  2      [ ]         DGRAM                     18223 
unix  3      [ ]         STREAM     CONNECTED      40500 
unix  3      [ ]         SEQPACKET  CONNECTED      26437 
unix  3      [ ]         SEQPACKET  CONNECTED      45464 
unix  2      [ ]         DGRAM                     20853 
unix  3      [ ]         STREAM     CONNECTED      19556 @/data/misc/fdbus/fdb-ns
unix  3      [ ]         SEQPACKET  CONNECTED      29361 
unix  2      [ ]         DGRAM                     28409 
unix  3      [ ]         SEQPACKET  CONNECTED      76343 
unix  3      [ ]         SEQPACKET  CONNECTED      75876 
unix  3      [ ]         STREAM     CONNECTED      17188 
unix  3      [ ]         SEQPACKET  CONNECTED      53618 
unix  3      [ ]         SEQPACKET  CONNECTED      53088 
unix  3      [ ]         STREAM     CONNECTED      26081 /dev/socket/netd
unix  3      [ ]         SEQPACKET  CONNECTED      20962 
unix  2      [ ]         DGRAM                     13116 
unix  2      [ ]         DGRAM                     10990 
unix  2      [ ]         DGRAM                     17642 
unix  3      [ ]         SEQPACKET  CONNECTED      50078 
unix  2      [ ]         DGRAM                     26766 
unix  2      [ ]         DGRAM                     12502 
unix  3      [ ]         STREAM     CONNECTED      45304 
unix  3      [ ]         SEQPACKET  CONNECTED      40496 
unix  3      [ ]         SEQPACKET  CONNECTED      24100 
unix  2      [ ]         DGRAM                     16566 
unix  3      [ ]         SEQPACKET  CONNECTED      76149 
unix  2      [ ]         DGRAM                     41290 
unix  2      [ ]         DGRAM                     18132 
unix  2      [ ]         DGRAM                     21635 
unix  3      [ ]         SEQPACKET  CONNECTED      76339 
unix  3      [ ]         SEQPACKET  CONNECTED      45300 
unix  3      [ ]         STREAM     CONNECTED      40505 
unix  2      [ ]         DGRAM                     26519 
unix  3      [ ]         SEQPACKET  CONNECTED      86764 
unix  3      [ ]         SEQPACKET  CONNECTED      76142 
unix  2      [ ]         DGRAM                     10836 
unix  2      [ ]         DGRAM                     24427 
unix  2      [ ]         DGRAM                     15533 
unix  3      [ ]         SEQPACKET  CONNECTED      46143 
unix  2      [ ]         DGRAM                     41073 
unix  3      [ ]         SEQPACKET  CONNECTED      27474 
unix  3      [ ]         STREAM     CONNECTED      12907 
unix  3      [ ]         SEQPACKET  CONNECTED      55604 
unix  2      [ ]         DGRAM                     18747 
unix  3      [ ]         SEQPACKET  CONNECTED      46420 
unix  3      [ ]         SEQPACKET  CONNECTED      29358 
unix  3      [ ]         SEQPACKET  CONNECTED     163617 
unix  3      [ ]         SEQPACKET  CONNECTED      30057 
unix  3      [ ]         SEQPACKET  CONNECTED      51419 
unix  2      [ ]         DGRAM                     14063 
unix  2      [ ]         DGRAM                     12912 
unix  2      [ ]         DGRAM                     41130 
unix  3      [ ]         SEQPACKET  CONNECTED      75882 
unix  3      [ ]         STREAM     CONNECTED      40909 /dev/socket/mdnsd
unix  3      [ ]         STREAM     CONNECTED      26101 
unix  2      [ ]         DGRAM                     20609 
unix  3      [ ]         SEQPACKET  CONNECTED      46400 
unix  3      [ ]         SEQPACKET  CONNECTED      26664 
unix  3      [ ]         SEQPACKET  CONNECTED      27354 
unix  3      [ ]         SEQPACKET  CONNECTED      29349 
unix  3      [ ]         SEQPACKET  CONNECTED      57369 
unix  3      [ ]         SEQPACKET  CONNECTED      53619 
unix  3      [ ]         SEQPACKET  CONNECTED      56479 
unix  3      [ ]         STREAM     CONNECTED      15836 
unix  2      [ ]         DGRAM                     41018 
unix  2      [ ]         DGRAM                     17344 
unix  2      [ ]         DGRAM                     18525 
unix  2      [ ]         DGRAM                     44663 
unix  3      [ ]         STREAM     CONNECTED      46205 
unix  2      [ ]         DGRAM                     13970 
unix  2      [ ]         DGRAM                     13751 
unix  3      [ ]         SEQPACKET  CONNECTED      54677 
unix  3      [ ]         STREAM     CONNECTED      45237 
unix  3      [ ]         STREAM     CONNECTED      31195 /data/misc/someip/172.16.3.99/vlan3-0
unix  3      [ ]         STREAM     CONNECTED      26102 /dev/socket/mdns
unix  3      [ ]         SEQPACKET  CONNECTED      24102 
unix  2      [ ]         DGRAM                     27001 
unix  3      [ ]         SEQPACKET  CONNECTED      76155 
unix  3      [ ]         SEQPACKET  CONNECTED      48286 
unix  3      [ ]         STREAM     CONNECTED      40332 
unix  2      [ ]         DGRAM                     41158 
unix  2      [ ]         DGRAM                     18767 
unix  3      [ ]         SEQPACKET  CONNECTED      29359 
unix  3      [ ]         SEQPACKET  CONNECTED      51602 
unix  3      [ ]         STREAM     CONNECTED      38887 
unix  3      [ ]         SEQPACKET  CONNECTED      29767 
unix  3      [ ]         SEQPACKET  CONNECTED      51420 
unix  3      [ ]         SEQPACKET  CONNECTED      46366 
unix  3      [ ]         STREAM     CONNECTED      16270 @/data/misc/fdbus/fdb-ns
unix  2      [ ]         DGRAM                     44363 
unix  2      [ ]         DGRAM                     14868 
unix  2      [ ]         DGRAM                     13740 
unix  3      [ ]         STREAM     CONNECTED      23586 
unix  2      [ ]         DGRAM                     12394 
unix  3      [ ]         SEQPACKET  CONNECTED     163618 
unix  2      [ ]         DGRAM                     76108 
unix  2      [ ]         DGRAM                     28624 
unix  2      [ ]         DGRAM                     17283 
unix  3      [ ]         SEQPACKET  CONNECTED      55603 
unix  2      [ ]         DGRAM                     30144 
unix  2      [ ]         DGRAM                     18092 

```




netstat services
```
:/mnt/vendor/persist #   netstat -plnt
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program Name
tcp        0      0 0.0.0.0:9090            0.0.0.0:*               LISTEN      10491/busybox
tcp        0      0 0.0.0.0:32098           0.0.0.0:*               LISTEN      4719/com.neusoft.na.navigation:Service
tcp        0      0 0.0.0.0:3490            0.0.0.0:*               LISTEN      376/dlt_daemon
tcp        0      0 0.0.0.0:22531           0.0.0.0:*               LISTEN      3472/com.neusoft.na.navigation
tcp        0      0 0.0.0.0:32099           0.0.0.0:*               LISTEN      4950/com.neusoft.na.navigation:OneCore
tcp        0      0 192.168.118.1:45635     0.0.0.0:*               LISTEN      330/tshregserver
tcp        0      0 192.168.118.1:47203     0.0.0.0:*               LISTEN      497/android.hardware.audio@2.0-service.rbgwm
tcp        0      0 0.0.0.0:22532           0.0.0.0:*               LISTEN      4719/com.neusoft.na.navigation:Service
tcp        0      0 0.0.0.0:5000            0.0.0.0:*               LISTEN      3905/com.ts.carplay
tcp        0      0 0.0.0.0:32042           0.0.0.0:*               LISTEN      4719/com.neusoft.na.navigation:Service
tcp        0      0 0.0.0.0:32044           0.0.0.0:*               LISTEN      4719/com.neusoft.na.navigation:Service
tcp        0      0 0.0.0.0:32046           0.0.0.0:*               LISTEN      4950/com.neusoft.na.navigation:OneCore
tcp        0      0 192.168.118.1:44399     0.0.0.0:*               LISTEN      530/vendor.bosch.log@1.0-service
tcp        0      0 0.0.0.0:8080            0.0.0.0:*               LISTEN      8531/busybox
tcp        0      0 0.0.0.0:1234            0.0.0.0:*               LISTEN      3905/com.ts.carplay
tcp        0      0 127.0.0.1:53            0.0.0.0:*               LISTEN      6903/dnsmasq
tcp        0      0 192.168.33.128:53       0.0.0.0:*               LISTEN      6903/dnsmasq
tcp        0      0 192.168.118.1:32981     0.0.0.0:*               LISTEN      529/vendor.bosch.lcm_controller@1.0-service
tcp        0      0 0.0.0.0:7000            0.0.0.0:*               LISTEN      3905/com.ts.carplay
tcp        0      0 0.0.0.0:22529           0.0.0.0:*               LISTEN      4950/com.neusoft.na.navigation:OneCore
tcp        0      0 192.168.118.1:37089     0.0.0.0:*               LISTEN      527/vendor.bosch.diag@1.0-service
tcp        0      0 192.168.118.1:60001     0.0.0.0:*               LISTEN      332/name-server
tcp        0      0 192.168.118.1:34206     192.168.118.2:65516     ESTABLISHED 493/bean_variant_server
tcp        0      0 192.168.118.1:45635     192.168.118.2:65465     ESTABLISHED 330/tshregserver
tcp        0      0 192.168.118.1:35466     192.168.118.2:65529     ESTABLISHED 497/android.hardware.audio@2.0-service.rbgwm
tcp        0      0 127.0.0.1:32044         127.0.0.1:64730         ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp        0      0 192.168.118.1:35388     192.168.118.2:65517     ESTABLISHED 638/vendor.bosch.hardware.automotive.vehicle@2.0-service
tcp        0      1 192.168.1.25:59186      34.120.195.249:443      FIN_WAIT1   -
tcp        0      0 192.168.118.1:35200     192.168.118.2:65515     ESTABLISHED 5356/com.bosch.lcm_time_track
tcp        0      0 192.168.118.1:46206     192.168.118.2:65534     ESTABLISHED 2412/com.autolink.clusterservice
tcp        0      1 192.168.1.25:44260      35.190.43.134:443       FIN_WAIT1   -
tcp        0      0 192.168.118.1:34202     192.168.118.2:65516     ESTABLISHED 333/variant_service
tcp        0      0 192.168.118.1:48652     192.168.118.2:65477     ESTABLISHED 4253/com.autolink.installer:InstallerManagerService
tcp        0      0 192.168.118.1:65184     192.168.118.2:65481     ESTABLISHED 524/smartservice
tcp        0      0 192.168.118.1:44120     192.168.118.2:65478     ESTABLISHED 2271/com.autolink.miscfdservice
tcp        0      1 192.168.1.25:41216      13.36.185.156:443       LAST_ACK    -
tcp        0      0 192.168.118.1:43806     192.168.118.2:60000     ESTABLISHED 332/name-server
tcp        0      0 192.168.118.1:63900     192.168.118.2:65495     ESTABLISHED 2271/com.autolink.miscfdservice
tcp        0      0 192.168.118.1:34590     192.168.118.2:65515     ESTABLISHED 2271/com.autolink.miscfdservice
tcp        0      0 127.0.0.1:22531         127.0.0.1:40988         ESTABLISHED 3472/com.neusoft.na.navigation
tcp        0      0 192.168.118.1:60001     192.168.118.2:65468     ESTABLISHED 332/name-server
tcp        0      0 127.0.0.1:32098         127.0.0.1:52428         ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp        0      0 127.0.0.1:64730         127.0.0.1:32044         ESTABLISHED 4950/com.neusoft.na.navigation:OneCore
tcp        0      0 127.0.0.1:32046         127.0.0.1:37816         ESTABLISHED 4950/com.neusoft.na.navigation:OneCore
tcp        0      0 192.168.118.1:38078     192.168.118.2:65518     ESTABLISHED 529/vendor.bosch.lcm_controller@1.0-service
tcp        0      0 127.0.0.1:22529         127.0.0.1:64308         ESTABLISHED 4950/com.neusoft.na.navigation:OneCore
tcp        0      1 192.168.1.25:54676      172.67.36.125:443       FIN_WAIT1   -
tcp        0      0 127.0.0.1:41090         127.0.0.1:32042         ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp        0      0 127.0.0.1:52428         127.0.0.1:32098         ESTABLISHED 4950/com.neusoft.na.navigation:OneCore
tcp        0      0 192.168.1.197:44058     162.14.21.56:853        ESTABLISHED 381/netd
tcp        0      0 192.168.118.1:49966     192.168.118.2:65496     ESTABLISHED 519/android.hardware.sensors@1.0-service
tcp        0      0 192.168.118.1:32981     192.168.118.2:65467     ESTABLISHED 529/vendor.bosch.lcm_controller@1.0-service
tcp        0      1 192.168.1.25:41234      13.36.185.156:443       LAST_ACK    -
tcp        0   5851 192.168.1.197:9090      192.168.1.27:59072      ESTABLISHED 10491/busybox
tcp        0      0 192.168.118.1:58190     192.168.118.2:65490     ESTABLISHED 527/vendor.bosch.diag@1.0-service
tcp        0      0 192.168.118.1:37728     192.168.118.2:65515     ESTABLISHED 333/variant_service
tcp        0      0 192.168.1.197:9090      192.168.1.27:58804      ESTABLISHED 10491/busybox
tcp        0      0 192.168.118.1:39000     192.168.118.2:65523     ESTABLISHED 528/vendor.bosch.display@1.0-service
tcp        0      1 192.168.1.25:45466      151.101.108.157:443     FIN_WAIT1   -
tcp        0      1 192.168.1.25:44258      35.190.43.134:443       FIN_WAIT1   -
tcp        0      0 192.168.1.197:60010     54.225.132.112:443      ESTABLISHED 5554/com.neusoft.na.navigation:Telematics
tcp        0      0 172.16.2.99:55001       172.16.2.97:55000       ESTABLISHED 377/vendor.ts.someip@1.0-service
tcp        0      0 192.168.118.1:62248     192.168.118.2:65489     ESTABLISHED 330/tshregserver
tcp        0      0 192.168.118.1:37089     192.168.118.2:65466     ESTABLISHED 527/vendor.bosch.diag@1.0-service
tcp        0      0 192.168.118.1:51626     192.168.118.2:65479     ESTABLISHED 530/vendor.bosch.log@1.0-service
tcp        0      0 192.168.118.1:59146     192.168.118.2:60001     ESTABLISHED 332/name-server
tcp        0      0 192.168.118.1:37738     192.168.118.2:65515     ESTABLISHED 523/gnss_publish
tcp        0      0 127.0.0.1:37816         127.0.0.1:32046         ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp        0      0 192.168.118.1:37742     192.168.118.2:65515     ESTABLISHED 524/smartservice
tcp6       0      0 :::22530                :::*                    LISTEN      5554/com.neusoft.na.navigation:Telematics
tcp6       0      0 :::5000                 :::*                    LISTEN      3905/com.ts.carplay
tcp6       0      0 :::22539                :::*                    LISTEN      4719/com.neusoft.na.navigation:Service
tcp6       0      0 :::29419                :::*                    LISTEN      2586/com.ts.car.power.ext.core
tcp6       0      0 :::9998                 :::*                    LISTEN      3873/com.ts.androidauto
tcp6       0      0 ::1:53                  :::*                    LISTEN      6903/dnsmasq
tcp6       0      0 fe80::280f:ebff:fe5e:53 :::*                    LISTEN      6903/dnsmasq
tcp6       0      0 :::23                   :::*                    LISTEN      553/busybox
tcp6       0      0 :::7000                 :::*                    LISTEN      3905/com.ts.carplay
tcp6       0      0 :::22559                :::*                    LISTEN      4719/com.neusoft.na.navigation:Service
tcp6       0      0 ::ffff:127.0.0.1:22530  ::ffff:127.0.0.1:33974  ESTABLISHED 5554/com.neusoft.na.navigation:Telematics
tcp6       0      0 ::ffff:127.0.0.1:41868  ::ffff:127.0.0.1:1234   ESTABLISHED 3905/com.ts.carplay
tcp6       0      0 ::ffff:127.0.0.1:22559  ::ffff:127.0.0.1:45606  ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp6       0    504 ::ffff:192.168.1.:45942 ::ffff:119.8.84.203:443 LAST_ACK    -
tcp6       0      0 ::ffff:127.0.0.1:22530  ::ffff:127.0.0.1:33940  ESTABLISHED 5554/com.neusoft.na.navigation:Telematics
tcp6       0      0 ::ffff:127.0.0.1:51714  ::ffff:127.0.0.1:22559  ESTABLISHED 3472/com.neusoft.na.navigation
tcp6       0      0 ::ffff:127.0.0.1:22539  ::ffff:127.0.0.1:53480  ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp6       0    515 ::ffff:192.168.1.:45940 ::ffff:119.8.84.203:443 LAST_ACK    -
tcp6       0      0 ::ffff:127.0.0.1:22559  ::ffff:127.0.0.1:45632  ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp6       0      0 ::ffff:127.0.0.1:45632  ::ffff:127.0.0.1:22559  ESTABLISHED 4719/com.neusoft.na.navigation:Service
tcp6       0      0 ::ffff:127.0.0.1:22530  ::ffff:127.0.0.1:33942  ESTABLISHED 5554/com.neusoft.na.navigation:Telematics
tcp6       0      0 ::ffff:127.0.0.1:45606  ::ffff:127.0.0.1:22559  ESTABLISHED 4719/com.neusoft.na.navigation:Service

```
Thank you.
