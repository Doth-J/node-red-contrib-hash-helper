# node-red-contrib-hash-helper :package: 

This is a subflow node for generating and verifying SHA digested hashes from user defined payload.

## Install :zap:
Run the following command in your Node-RED user directory - typically `~/.node-red`

        npm install node-red-contrib-hash-helper

## Generator API :gear:

- :information_source: **POST localhost:1880/generate**

The __data__ payload can be either a string or an object, you must define the __function__ to use (``SHA``/``HMAC``) and the __version__ of the algorithm (``1/224/256/384/512/3``)

![GeneratorAPI](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/GeneratorAPI.PNG)

### Generating Hash :inbox_tray: :arrow_right:
* Setting the payload of the **Generate Hash** injector:

![SHA1](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/SHA1.PNG)

#### Hash Result :receipt: :back:
* Hash response payload:
  
![SHA2](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/SHA2.PNG)

---

### Generating HMAC :inbox_tray: :arrow_right:
:warning: In the case of ``HMAC``, the __key__ parameter must also be set!  

* Setting the payload of the **Generate Hash** injector:

![HMAC1](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/HMAC1.PNG)

#### HMAC Result :receipt: :back:
* HMAC response payload:

![HMAC2](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/HMAC2.PNG)

## Verifier API :toolbox:

- :information_source: **POST localhost:1880/verify**

The __data__ payload can be either a string or an object, you must define the __function__ to use (``SHA``/``HMAC``), the __version__ of the algorithm (``1/224/256/384/512/3``) and the __hash__ to verify.

![VerifierAPI](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/VerifierAPI.PNG)

### Verifying Hash :inbox_tray: :arrow_right:
* Setting the payload of the **Verify Hash** injector:

![SHA3](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/SHA3.PNG)

#### Hash Verification Result :receipt: :back:
* Hash response payload:
  
![SHA4](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/SHA4.PNG)

---

### Verifying HMAC :inbox_tray: :arrow_right:
:warning: In the case of ``HMAC``, the __key__ parameter must also be set!  

* Setting the payload of the **Verify Hash** injector:

![HMAC3](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/HMAC3.PNG)

#### HMAC Verification Result :receipt: :back:
* HMAC response payload:
  
![HMAC4](https://github.com/Doth-J/node-red-contrib-hash-helper/blob/master/docs/HMAC4.PNG)
