## Writeup for Macro Trace

Given to us is the excel sheet with an embedded macro in it along with the windows event viewer file

flag: `UMASS{drop_it_like_its_hot}`

### Solution

Going through the evtx file, we see that a script was run to print fake statements like health condition and suspicious string with some random characters. But before all of this, we can see a base64 encoded string "VU1BU1N7ZHJvcF9pdF9saWtlX2l0c19ob3R9".

Decoding this reveals the flag. This is placed in between the obfuscation health check statement and suspicious command statement.
