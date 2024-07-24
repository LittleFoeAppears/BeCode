## Zeek

- Type of Challenge: Analysis 
- Duration: 3 days
- Challenge type : Solo

Learning Outcome - Familiarization with Zeek, its basic usage and simple scripting capabilities.

## Tasks

1. Install Zeek.
2. Run Zeek to monitor traffic on the chosen interface.
3. Zeek will create log files in the current directory. List the files to see the generated logs.
4. Inspect the **conn.log** file. Use any text editor. Identify some key fields like **ts, id.orig_h, id.resp_h, proto, duration, orig_bytes, resp_bytes**.
5. Explore Sample Scripts. Zeek comes with several sample scripts located generally in the **/usr/share/zeek/scripts** directory. Explore these scripts to get a feel for the syntax and functionalities.
6. Create a Zeek script. Create a new file named **test-conn.zeek**. Write the script to print a message when a connection is established.
7. Execute the script with Zeek on a pcap file or live traffic. If you don't have a pcap file, you can download a sample one from Wireshark Sample Captures or use a Wireshark pacap from your own capture.
8. Modify the script **test-conn.zeek** script to log connection details to a custom log file.
9. Execute the script on the same pcap file or live traffic.
10. Verify that the custom log file **tset-conn.log** is created and contains the expected connection information.

## Documentation

1. Explain in details your methodology.
2. Zeek scripts.

## [Group project](./Zeek2.md) 

