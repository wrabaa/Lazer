import RPi.GPIO as GPIO
import time

# Set the GPIO mode
GPIO.setmode(GPIO.BCM)

# Define the GPIO pin for the laser module
trig_pin = 18

# Set up the laser module pin
GPIO.setup(trig_pin, GPIO.OUT)

def activate_laser():
    # Turn on the laser by setting the GPIO pin to HIGH
    GPIO.output(trig_pin, GPIO.HIGH)

def deactivate_laser():
    # Turn off the laser by setting the GPIO pin to LOW
    GPIO.output(trig_pin, GPIO.LOW)

try:
    while True:
        # Activate the laser for 1 second
        activate_laser()
        time.sleep(1)

        # Deactivate the laser for 1 second
        deactivate_laser()
        time.sleep(1)

except KeyboardInterrupt:
    pass

finally:
    # Clean up GPIO settings
    GPIO.cleanup()
