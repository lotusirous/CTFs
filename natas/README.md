# Natas


- level 1: view-source ctrl+u. ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi 
- level 2: No thing on this page: http://natas2.natas.labs.overthewire.org/files/users.txt => natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
- level 3: `<!-- No more information leaks!! Not even Google will find it this time... -->` robots.txt => natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
- level 4: Referer ```Access granted. The password for natas5 is iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq ```
- level 5: cookie login ```Access granted. The password for natas6 is aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1```
- level 6: Access granted. The password for natas7 is 7z3hEENjQtflzgnT29q7wAvMNfZdh0i9 
- level 7: file include. DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe 
- level 8: decode

``` <?php
$encodedSecret = "3d3d516343746d4d6d6c315669563362";
function decode_secret($encoded){
    echo base64_decode(strrev(hex2bin($encoded)));
}

decode_secret($encodedSecret);

?>
```

password: oubWYf2kBq => natas9: W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl

- level 9: command include in `grep -i $key dictionary.txt. Attack vector: `None dictionary.txt; cat /etc/natas_webpass/natas9; ls` : W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl
