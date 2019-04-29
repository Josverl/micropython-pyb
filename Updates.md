Changes 

class ADC : 
    def read_timed(self, buf, timer):

    Was defined twice in the same class
    Corrected and remaining defenition matched http://docs.micropython.org/en/latest/library/pyb.ADC.html

class CAN:
    def clearfilter(self, bank):

    missing self parameter 
    matches documentation http://docs.micropython.org/en/latest/library/pyb.CAN.html

Class DAC:
    def deinit(self):
    missing self parameter 

Class Pin:
    was : def af_list(cls,):
    
    the documentation is very sparse 
    ```
    Pin.af_list()
    Returns an array of alternate functions available for this pin.
    ```
    based on the use of cls rather than self, it could be that it is actuall missing a  @classmethod
    but I do not have the hardware to verify this one way or another.

    updated to :
    ```
        @classmethod
        def af_list(cls):
            """
            Returns an array of alternate functions available for this pin.
            """
            pass
        ``` 

class Switch:
    def __call__(self):

    missing self parameter 
    matches documentation http://docs.micropython.org/en/latest/library/pyb.Switch.html

Class USB_HID: 
    def send(self, data):

    missing self parameter 
    matches documentation http://docs.micropython.org/en/latest/library/pyb.USB_HID.html

Miscelanious:
    adjusted whitespace where needed

