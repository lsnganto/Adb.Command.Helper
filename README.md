# Adb.Command.Helper
[![NuGet](https://img.shields.io/nuget/v/Adb.Command.Helper.svg?maxAge=86400&style=flat)](https://www.nuget.org/packages/Adb.Command.Helper/)
## Usage

    // setting ADB folder path
    CommandHelper.ADBHelper.SetADBFolderPath(Application.StartupPath + @"\")
    
## Get devices
    var devices = CommandHelper.ADBHelper.GetDevices();
    
## Open App
    var deviceId = "127.0.0.1:xxxxx";
    var app = "com.xxx.xxx";
    CommandHelper.ADBHelper.OpenApp(deviceId, app);
    
## Check app running 
    var deviceId = "127.0.0.1:xxxxx";
    var app = "com.xxx.xxx";
    var isRun = CommandHelper.ADBHelper.CheckAppRunning(deviceId, app);
    
## Tap screen
    var deviceId = "127.0.0.1:xxxxx";
    var x = 100;
    var y = 100;
    CommandHelper.ADBHelper.Tap(deviceId, x, y);
    
 ## Swipe screen
    var deviceId = "127.0.0.1:xxxxx";
    var x1 = 100;
    var y1 = 100;
    var x2 = 200;
    var y2 = 200;
    var duration = 500;
    CommandHelper.ADBHelper.Swipe(deviceId, x1, y1, x2, y2, duration);

## ScreenShoot
    var deviceId = "127.0.0.1:xxxxx";
    var isDeleteImageAfterCapture = false;
    var screen = CommandHelper.ADBHelper.ScreenShoot(deviceId, isDeleteImageAfterCapture);
    
## FindOutPoint image in screen
    public Point FindPoint(Bitmap source){
      var deviceId = "127.0.0.1:xxxxx";
      var screen = CommandHelper.ADBHelper.ScreenShoot(deviceId, false);
      return CommandHelper.ImageScanOpenCV.FindOutPoint(screen, source);
    }
    
## InputText
    var deviceId = "127.0.0.1:xxxxx";
    var text = "abcd";
    CommandHelper.ADBHelper.InputText(deviceId, text);
