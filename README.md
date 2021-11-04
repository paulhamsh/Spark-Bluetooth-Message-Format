# Spark-Bluetooth-Message-Format

Details of the bleutooth messages sent between the app and the amp.   

Overall, a bit of SysEx and msgpack, but a bit broken too   
And amp to app data can be unreliable so code defensively assuming it will be broken   


Version updates   
v1.2 - added that the byte after the sequence number in the chunk header is an 8bit xor of the actual data (between header and trailing f7). The app seems sensitive to this but the amp does not seem to use it.    

v1.4 - now includes details on the checksum, recall preset 0x0100 retrieves actual amp current state, and some other corrections.    

v2.0 - includes preset checksum so now a *complete* preset description   

v3.0 - includes the new 0x022a preset comparison message and the 0x0170 license key message, other updates to tidy up the document

Example v1.0 - this shows a worked example of how to create a preset from the raw data in C form   

