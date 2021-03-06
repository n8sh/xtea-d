xtea-d [![Build Status](https://travis-ci.org/Extrawurst/xtea-d.svg)](https://travis-ci.org/Extrawurst/xtea-d) [![Coverage Status](https://coveralls.io/repos/Extrawurst/xtea-d/badge.svg?branch=master)](https://coveralls.io/r/Extrawurst/xtea-d?branch=master) [![version](https://img.shields.io/dub/v/xtea-d.svg)](https://code.dlang.org/packages/xtea-d) [![downloads](https://img.shields.io/dub/dt/xtea-d.svg)](https://code.dlang.org/packages/xtea-d)
======

XTEA cryptography algorithm implementation in D (eXtended Tiny Encryption Algorithm)

usage:
------

This is a dub library (http://code.dlang.org/about). Just add dependancy to your package.json:

```
{
	...
	"dependencies": {
		"xtea-d": "~>0.1.0",
		...
	}
}
```

A simple source code example is in the provided app.d and looks like this:

```
import xtea.XteaCrypto;

void main()
{ 
	auto crypto = XTEA([1,2,3,4], 64);

	auto data = [0,1,2,3,4,5,6,7];

	writefln("data:\t%s",data);
	
	crypto.Encrypt(data);

	writefln("encrypted:\t%s",data);
}
```
