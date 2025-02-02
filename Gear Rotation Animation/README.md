# Gear Rotation U8glib library

Explanation:

Gear Drawing: The drawGear function uses trigonometry to calculate the positions of the gear teeth and draws them using u8g.drawLine. It also draws inner and outer circles to represent the gear's body.

Rotation: The angle variable rotates the gear by a fixed step (angleStep) on each frame. The loop function continuously redraws the gear with the updated angle. 
angle increments by angleStep1 (+5 degrees per frame) to rotate clockwise.
angleCC decrements by angleStepCC (-5 degrees per frame) to rotate counterclockwise

Frame Rate: You can adjust the delay() to control the speed of the animation. The delay(50) makes the frame rate faster (previously delay(100)), making the overall animation smoother and quicker.

Angle Direction: The angleStep is set to 5, making the gear rotate clockwise. And the angleStepCC is set to -5, making the gear rotate counter-clockwise.
Set to 15 and -15 degrees (previously 5 degrees). This increases the rotation amount per frame, making the gears spin faster.

Angle Wrapping: The if (angle < 0) condition ensures the angle wraps around to stay within [0, 360) when decrementing. Angles are kept within [0, 360) to avoid overflow or underflow for both gears.

Notes:

This code assumes an 8-tooth gear for simplicity. You can adjust the number of teeth by changing the numTeeth value.

The gear rotates smoothly by incrementing/decrementing the angle in small steps (angleStep)/(angleStepCC).

This code will now rotate the gears in directions (counterclockwise and clockwise). You can adjust the speed by modifying the delay(100) value or changing the magnitude of angleStep/angleStepCC.

## Upload this code to your microcontroller, and you should see 3 rotating gear animation on your OLED display!
