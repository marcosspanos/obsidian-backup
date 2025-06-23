# general purpose vs shallow classes:
a common decision is whether to make your module in a general purpose or a special purpose manner
general purpose allows to address broad range of problems not just the ones of today
special purpose argues that the needs of the future are hard to know so there might be functions which are not needed at all in the end

## somewhat general purpose
the modules functionality should reflect your current needs but the interface should not 
the interface should be general enough to support multiple uses 
## generality leads to better information hiding 
general purpose approach provides a cleaner separation between the text adn the user interface
new user interface features can be added without creating new supporting functions in the class
