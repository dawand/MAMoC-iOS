# MAMoC (Multisite Adaptive Mobile Cloud)
A Swift framework for running compute-intensive tasks on nearby devices, cloudlets, and remote clouds. This framework uses MultiPeer Connectivity(MPC) to discover other devices over standard LAN and ad-hoc peer-to-peer WiFi or Bluetooth networks to offload computation. It also allows devices to connect to nearby fixed servers (cloudlets) or remote cloud servers and communicate over a socket.

### Text Search Example
```Swift
// start the framework
let mc = MobileCloud.MCInstance
mc.start()
// set the job
mc.setJob(job: TSJob())
// set the parameters
(mc.getJob() as! TSJob).searchTerm = textSearchField.text!
// execute the job on nearby, cloudlet, remote cloud, or auto (let MAMoC decide)
mc.execute(type: OffloadingType.auto)
```

There are two working examples provided as app targets when you open the XCode project. 

For setting up the container on both cloudlet and remote clouds check the [documentation](https://github.com/dawand/MAMoC/wiki/Documentation).

## Installation

### Cocoapods
TBD

### Manual
TBD


## Open source third party libraries
- [PeerKit](https://github.com/jpsim/PeerKit) (An open-source Swift framework for building event-driven, zero-config Multipeer Connectivity apps)
- [Starscream](https://github.com/daltoniam/Starscream) (Websockets in swift for iOS and OSX)
- [SwiftEventBus](https://github.com/cesarferreira/SwiftEventBus) (A publish/subscribe EventBus optimized for iOS)
- [Luminous](https://github.com/andrealufino/Luminous) (iOS system information )
- [iOS-System-Services](https://github.com/Shmoopi/iOS-System-Services) (iOS System Services is a class to gather all available information about a device.)
- [Vapor](https://github.com/vapor/vapor) (A server-side Swift web framework)

## TODO

- [x] Cloudlet setup on local and remote servers
- [ ] Cloudlet container migration for user mobility
- [ ] Document the API
