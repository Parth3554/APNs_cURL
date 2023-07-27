# APNs_cURL
Test push notifications using the terminal.

Test your development .pem certificate using following command.
/usr/local/Cellar/curl/7.54.1/bin/curl -v \
-d '{"aps":{"alert":"test","sound":"default"}}' \
-H "apns-topic:com.yourcompanyname.yourappname" \
-H "apns-expiration: 1" \
-H "apns-priority: 10" \
--http2 \
--cert yourpempath:yourpempassword \
https://api.development.push.apple.com/3/device/yourdevicetoken

Test your production .pem certificate using following command.
/usr/local/Cellar/curl/7.54.1/bin/curl -v \
-d ‘{“aps”:{“alert”:”test”,”sound”:”default”}}’ \
-H “apns-topic:com.yourcompanyname.yourappname” \
-H “apns-expiration: 1” \
-H “apns-priority: 10” \
 — http2 \
 — cert yourpempath:yourpempassword \
https://api.push.apple.com/3/device/yourdevicetoken
