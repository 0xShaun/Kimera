# Kimera

Welcome to Kimera.

[![Build Status](https://travis-ci.org/maxoly/Kimera.png?branch=master)](https://travis-ci.org/maxoly/Kimera)

## Disclaimer
All code on this repository is for educational purposes only and is not intended for production code. 
The code is supplied "as is". Use at your own risks.

## Project Architecture

### Folder Structure

* KimeraMobile: contains all project files and resources.
    * Application: contains all file related to main, UIApplication, AppDelegate and project plist
        * change Build Settings -> Info Plist file (INFOPLIST_FILE) for plist file
        * change Build Settings -> Prefix Header (GCC_PREFIX_HEADER)
        
## Advanced Debugging

### Use Marco

Don't use NSLog, instead use a simple macro


```
#if defined DEBUG
    #define KRMLog(s, ...) NSLog((@"%s [Line %d] " s), __PRETTY_FUNCTION__, __LINE__, ##__VA_ARGS__)
#else
    #define KRMLog(s, ...)
#endif


