This is a simple sample project to show the issue I'm having building my framework test target using `OTXCFramework` versions 2.25.2 and 2.25.3 via Cocoapods

To test, open the .xcworkspace file and run the tests (<cmd>+u). You should get a crash as the tests start refereing to `#0	0x00000001434148a0 in google::LogMessage::Init(char const*, int, int, void (google::LogMessage::*)()) ()`

If you downgrade the version in the `Podfile` to 2.25.1 and run `pod update` then run the test, everything passes
