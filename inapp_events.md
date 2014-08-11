# In-App events

### Viewed 'popular' tab on homescreen
```
NSDictionary *dimensions = @{
    @"loc" : @"home",
    @"pos" : @"tab",
    @"target" : @"popular"  
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Viewed 'mine' tab on homescreen
```
NSDictionary *dimensions = @{
    @"loc" : @"home",
    @"pos" : @"tab",
    @"target" : @"mine"  
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Tapped image on homescreen
```
NSDictionary *dimensions = @{
    @"loc" : @"home",
    @"pos" : @"{id}",
    @"target" : @"image"  
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Tapped 'create' button
```
NSDictionary *dimensions = @{
    @"loc" : @"home|image|reply",
    @"pos" : @"button",
    @"target" : @"create"  
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Tapped 'reply' button
```
NSDictionary *dimensions = @{
    @"loc" : @"image",
    @"pos" : @"button",
    @"target" : @"reply",
    @"to" : @"{id}",
    @"depth" : @"0"
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Tapped image reply (tier 1)
```
NSDictionary *dimensions = @{
    @"loc" : @"image",
    @"pos" : @"button",
    @"target" : @"reply",
    @"to" : @"{id}",
    @"depth" : @"1|2|3|4|5|..."
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Viewed create screen
```
NSDictionary *dimensions = @{
    @"loc" : @"create",
    @"pos" : @"button",
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Chose a font
```
NSDictionary *dimensions = @{
    @"loc" : @"font",
    @"pos" : @"select",
    @"target" : @"{fontname}"
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Used background template 
```
NSDictionary *dimensions = @{
    @"loc" : @"font",
    @"pos" : @"select",
    @"target" : @"{fontname}"
};
[PFAnalytics trackEvent:@"tab", dimensions: dimensions];
```

### Chose image search
### Ran manual search query for image
### Removed background image
### Viewed post screen
### Connected twitter account
### Connected facebook account
### Shared on Stationery
### Shared on Twitter
### Shared on facebook
### Shared via email
### Shared via text
### Saved to camera roll
### Copied link to clipboard
### Deleted image from 'mine' tab
### Time (Minutes : seconds) user spends in app
### Time (Minutes : seconds) user spends in each view
### After what event is the app closed (want to understand any issues/errors/events that are leading to people leaving the app)?












