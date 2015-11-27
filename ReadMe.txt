### FullScreenWindow ###

===========================================================================
DESCRIPTION:

Demonstrates how to use Full-Screen APIs with NSWindow, complete with custom animation effects.

Here is a checklist of items to consider when adopting first full-screen:

1) Specify which windows can be made full screen by setting the collection behavior in the xib or programmatically.

2) Add an "Enter Full Screen" menu item to the View menu. If you don't have a View menu, the Window menu is a good alternative.  Interface Builder provides you with a template "Full Screen Menu Item".  Specifically it has "toggleFullScreen:" as the action, and nil as the target.  The short cut is "Ctrl-Command-F".  

3) Consider auto-hiding your window's toolbar, if you have one.

4) Customize the window's full screen size if necessary.


The sample also shows how to implement the following delegate methods -

To override the window's full screen content size:
- (NSSize)window:(NSWindow *)window willUseFullScreenContentSize:(NSSize)proposedSize;

To determine the presentation options the window will use when transitioning to full-screen mode:
- (NSApplicationPresentationOptions)window:(NSWindow *)window willUseFullScreenPresentationOptions:(NSApplicationPresentationOptions)proposedOptions;

To use NSNotificationCenter for NSWindowDidEnterFullScreenNotification and NSWindowDidExitFullScreenNotification to detect when the window goes in and out of full-screen.

To customize the window full screen animation using:
- (void)window:(NSWindow *)window startCustomAnimationToEnterFullScreenWithDuration:(NSTimeInterval)duration;
- (void)window:(NSWindow *)window startCustomAnimationToExitFullScreenWithDuration:(NSTimeInterval)duration;

As a side note if you want to directly put its window into and out of full-screen, you use this:
    [self.window toggleFullScreen:self];

===========================================================================
BUILD REQUIREMENTS:

Mac OS X 10.7 or later

===========================================================================
RUNTIME REQUIREMENTS:

Mac OS X 10.7 or later

===========================================================================
CHANGES FROM PREVIOUS VERSIONS:

Version 1.0
- First version.

===========================================================================
Copyright (C) 2011 Apple Inc. All rights reserved.
