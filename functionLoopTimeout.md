```
var obj = {
    cancel: false, // for breaking dots while sending

    sendingNotification: function() {
        var speed = 300
            var maxDots = 3
            var that = obj

            var cancelled = that.cancel
            var button = '[data-booking-destination="submit"]'
            var sendingTxt = '[data-booking-sendingNotification]'

            // breaking loop if canceled
            if(cancelled){
                return
            }

        // DOING JOB

        // animate sending button
        if( that.sendingButton.dot < maxDots){
            $(button).append(' . ')
                that.sendingButton.dot ++
        } else {
            $(button).text('')
                that.sendingButton.dot = 0
        }

        // loop it, speed in ms
        if (!cancelled) {
            setTimeout(that.sendingNotification, speed);
        }
    }
}
```

= functional =
```
var running = true
function loop_slides() {
    // breaking loop if canceled
    if(!running){
        console.log('stop')
            return
    }
    // DOING JOB
    console.log('loop')
        hide_items(selectors.items)
        show_item(current_item)
        update_state()
        // loop it, speed in ms
        if (running) {
            setTimeout(loop_slides, speed);
        }
}
```

= setInterval pause =
```
var isRunning = true
function loop_slides(){
    interval = setInterval(function(){ //jshint ignore: line
            if(isRunning){
            hide_items(selectors.items)
            show_item(current_item)
            update_state()
            }
            },speed)
}
```
