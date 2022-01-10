Day 9 [Networking]


1 - GET requests section, which directory if found on the web server?
    a. Filter results to only show HTTP GET requests with "http.method.request == GET"
    b. In packet 725 we can see "GET /login HTTP/1.1" which tells us that "login" is the directory found on the server

2. What is the username and password used in the login page in the HTTP #2 - POST section?
    a. Filter "http.request.method == POST"
    b. Packet 725 contains username and password under "HTML Form URL Encoded"

3. What is the User-Agent's name that has been sent in HTTP #2 - POST section?
    a. In the same packet used in 1a we can dig deeping into the packet and find the UserAgent flag

4. In the DNS section, there is a TXT DNS query. What is the flag in the message of that DNS query?
    a. Filter results to "udp.port == 53" which will show all DNS packets
    b. Search for filter with TXT packet in
    c. Right-click and select "follow -> UDP Stream" to find flag

5. In the FTP section, what is the FTP login password?
    a. Set filter to "ftp"
    b. Look for packet that follows "Please specify password"

6. In the FTP section, what is the FTP command used to upload the secret.txt  file?
    a. Keep filter as "ftp"
    b. Right-click on first ftp packet and selecet "follow -> TCP stream"
    c. Look for command that involves "secret.txt"

7. In the FTP section, what is the content of the secret.txt file?
    a. Set filter to "ftp-data" which will result only 1 packet
    b. Find AoC Flag within that packet

Congratulations!
