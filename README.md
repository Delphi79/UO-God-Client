# UO-God-Client

A non encrypted 2.0.8n Godclient with additional unknown modifications. The god client is a special client used by staff members to more efficiently carry out their jobs.

Perhaps the most interesting feature of the god client is its ability to directly alter the mul files, including maps and statics. As far as I know, I'm the first non-OSI developer to discover the key to unlocking this feature :) In order to enable editing, you must do the following:

1. Add the line "EditServer=127.0.0.1,8558" to the uo.cfg file, where 127.0.0.1 is the server address and 8558 is the port.
2. Enable login encryption for the god client. Its keys are 0x2CD3257D and 0xA37F527F.
3. Note that when the client connects to an Edit Server, it does NOT send the usual encryption seed packets.
4. Make sure you send the proper information in the Login Confirm packet. Note that there is new information for this packet that must be included to enable editing without causing client-side errors.
5. Be aware that packets used with newer client versions may cause errors or freezing for the 2.0.8n god client.
6. Turn on God Mode through the God Mode packet.

After adding the EditServer entry in uo.cfg, the client will only be able to login to an Edit Server until the entry is removed. The address in the EditServer entry must also be in the login.cfg file. After successfully logging in to the Edit Server, the mul updating packets such as Update Statics and Update Terrain will cause the client's files to be altered.

This was taken from http://necrotoolz.sourceforge.net/
