base64_javascript_test_data
===========================


I have some image data (source was NSData in iOS) that has been already base 64 encoded. I used the functions at

http://ntt.cc/2008/01/19/base64-encoder-decoder-with-javascript.html

to decode and then encode and the result was not the same as the original. I used an MD5 hash for a quick compare (hex_md5 function from code at http://pajhome.org.uk/crypt/md5/instructions.html).

I then tried some equivalent base 64 routines from http://phpjs.org/functions/base64_decode/ and http://phpjs.org/functions/base64_encode/ These routines provided the correct result when I tried the decode/encode loop.

My base 64 encoded test case string is located in the file base64_data.

The hash of the base 64 encoded input (and the expected hash result after the decode/encode) is e506287b79051b4fa3fba38a2bc70e90 What I get with the routines at ntt.cc (first reference above) after the decode/encode is 98778254fccc18951a3d876045a7ebd6.   The routines at phpjs.org gave me the expected hash result.

