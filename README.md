# Spark-Bluetooth-Message-Format

Details of the bleutooth messages sent between the app and the amp.

Overall, a bit of SysEx and msgpack, but a bit broken too
And amp to app data can be unreliable so code defensively assuming it will be broken


Version control.
v1.2 - added that the byte after the sequence number in the chunk header is an 8bit xor of the actual data (between header and trailing f7). The app seems sensitive to this but the amp does not seem to use it.   
