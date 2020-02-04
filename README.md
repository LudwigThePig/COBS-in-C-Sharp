# Consistent Overhead Byte Stuffing

This repo contains a C# implementaiton of the COBS algorithm.

## Usage

```cs
using COBSNS;

// ...

int[] bytesToEncode = {0x00, 0x00};
int[] encodedBytes = COBS.Encode(bytesToEncode); // {0x01, 0x01}
int[] encodedWithNullTerminator = COBS.Encode(bytesToEncode); // {0x01, 0x01, 0x00}

int[] bytesToDecode = {0x01, 0x01};
int[] decodedBytes = COBS.Decode(bytesToEncode);
// ...  
```


## Unit Tests

There are twenty unit tests, ten for encoding and ten for decoding. The unit tests test against the examples given in the [wikipedia article on COBS](https://en.wikipedia.org/wiki/Consistent_Overhead_Byte_Stuffing#Encoding_examples).

