Install
========

First, make sure Xcode is not running.  Then do:

```
git clone git@github.com:rubymaverick/XcodeCodeSnippets.git ~/Library/Developer/Xcode/UserData/CodeSnippets
```

To confirm they've been installed, open Xcode's Code Snippet sidebar:

![snippets](http://f.cl.ly/items/1r2u1V20201P1m191s0g/snippets.png)

Usage
======

#### kiftest

```
KIFTestCondition(<#test condition#>, error, ERROR(<#error identifier#>));
```

#### kifdef

```
return [KIFTestStep stepWithDescription:@"Testing something"
        executionBlock:^(KIFTestStep *step, NSError **error) {
        // Test setup
                                 
            
                                 
        return KIFTestStepResultSuccess;
    }];
```

#### swizzleCat

```
@interface <#class to swizzle#> (SwizzlingMethods)
<#custom method interface#>
@end

@implementation <#class to swizzle#> (SwizzlingMethods)
<#custom method interface#>
{
    <#custom implementation#>
    
    // send custom message to self
    // and return if this method has a return
    // value
}
@end
```

#### swizzleIMethod

```
[CSSwizzler swizzleClass:<#class object#>
           replaceMethod:@selector(<#original method#>)
              withMethod:@selector(<#custom method#>)];
```

#### swizzleCluster

```
[CSSwizzler swizzleClassOfInstance:<#instance#>
                      replaceMethod:@selector(<#original#>)
                         withMethod:@selector(<#replacement#>)];
```

#### testingapp

```
TestingAppDelegate *appDel = [[UIApplication sharedApplication] delegate];
```

