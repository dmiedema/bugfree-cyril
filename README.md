bugfree-cyril
=============

Test repository for demonstration



---------



# How to actually use these

Go to File->New->File->Resource->Settings Bundle

1. Replace the contents of *Root.plist* with the contents of this Gists *Root.plist*. 
2. Add whatever other fields you want
3. Put the following inside your *AppDelegate.m* file to have the Version/Build set from the apps current settings

``` objectivec
    /* Settings App Bundle */
    NSString *build = [[[NSBundle mainBundle] infoDictionary] objectForKey:@"CFBundleVersion"];
    [[NSUserDefaults standardUserDefaults] setObject:build forKey:@"build_preferences"];
    NSString *verison = [[[NSBundle mainBundle] infoDictionary] objectForKey:@"CFBundleShortVersionString"];
    [[NSUserDefaults standardUserDefaults] setObject:verison forKey:@"version_preferences"];
```

4. ?????
5. Profit
 
