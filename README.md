# PHP BaseX - Any Base Encoding/Decoding

ported from [js base-x](https://github.com/cryptocoinjs/base-x)

## Installation

`composer require brtnetwork/base-x`

## Usage

In below sample used ripple alphabet to encode and decode ripple base58 address and seed

```
require_once 'vendor/autoload.php';

use BRTNetwork\BaseX\BaseX;

$brtAlphabet = 'brtshnaf39wBUDNEGHJKLM4PQRST7VWXYZ2pcdeCg65jkm8oFqi1uvAxyz';
$basex          = new BaseX($brtAlphabet);

// BRT Address Encode/Decode
$addressDecode = $basex->decode('r9LqNeG6qHxjeUocjvVki2XR35weJ9mZgQ');
var_dump($addressDecode->getHex());    // 005B812C9D57731E27A2DA8B1830195F88EF32A3B6FCBFC92D

$addressEncode = $basex->encode($addressDecode);
var_dump($addressEncode); // r9LqNeG6qHxjeUocjvVki2XR35weJ9mZgQ

// BRT Seed Encode/Decode
$seedDecode = $basex->decode('sp5fghtJtpUorTwvof1NpDXAzNwf5');
var_dump($seedDecode->getHex());    // 210102030405060708090A0B0C0D0E0F10208988A1

$seedEncode = $basex->encode($seedDecode);
var_dump($seedEncode); // sp5fghtJtpUorTwvof1NpDXAzNwf5
```
