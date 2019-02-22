# Read SMS from Serial Port Cellular LTE Modem

Read SMS Messages

Makes a serial connection to a Quectel EC25 LTE modem chipset...

  https://www.quectel.com/product/ec25.htm
  
via Raspberry Pi Hat from SixFab.com..
  
  https://sixfab.com/product/raspberry-pi-3g-4glte-base-shield-v2/
  
and Sixfab.com PCIe module...

  https://sixfab.com/product/quectel-ec25-mini-pcle-4glte-module/
  
Cellular Info
-------------

Country: Canada (Sudbury Ontario)
Micro SIM Service Provider: Rogers.com
Band: North America
APN: ltemobile.apn
Rogers: mms.gprs.rogers.com
Port: /dev/ttyUSB3
  
  
USAGE
-----

optional arguments:

  -h, --help            show this help message and exit


  Read SMS Messages
  --------------------
  
  -h, --help            show this help message and exit
  
  -ra, --readall        Read all the SMS messages recieved
  
  -raw, --readallraw    Read all the SMS message and display raw output
  
  -r READN, --readn READN
  
                        Read SMS by ID
                        
  -s SEARCH, --search SEARCH
  
                        Search 'from', 'message', and 'datetime' fields in messages. Regex can my used.
                        
                        FYI: '(?i)' in regex expression will turn off case sensitive
                        
  -k KEY, --key KEY     Return key field only from Search
  
                        ie. -s 'hello' -k 'from'.
                        
                        Search returns only 'from' field
                        
  -rl [READLASTN], --readlastn [READLASTN]
  
                        Display the last N sms messages.
                        
                        Default: Last 1 message
                        
  -ls, --lastsearch     Show the messages made with the last search command
  
  -sl, --showlist       Show the IDs of the messages made with the last command
  
  --shortcodes          Show all messages from shortcode phone numbers 4-6 digits
  
  -DEL DELETEN, --deleten DELETEN
  
                        Delete SMS by ID
                        
  -DALL, --deleteall    Delete all the SMS messages recieved
  
  -DLIST, --deletelist  Delete ALL the message IDs in --lastsearch list
  
  -DL [DELETELASTN], --deletelastn [DELETELASTN]
  
                        Delete the last N messages by date ONLY (Ascending)
                        
  -p PATH, --path PATH  
  
                        Default File Path: mms/modem_tmp_files/
                        
                        Files must be in the above directories unless otherwise specified.
                        
  -b BAUDRATE, --baudrate BAUDRATE
  
                        Default: 115200
                        
  -o PORT, --port PORT  Default: /dev/ttyUSB3
  
  -d, --debug           Default: False
  
  --json                Output results as json [Default]
  
  --text                Output results as text

