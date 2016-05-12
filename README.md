# Milight RF reversing

TODO

## Specs

 * Frequency: 2.406GHz, 2.441GHz, 2.476GHz
 * Modulation: 2FSK
 * Symbol rate: 1Mbaud

## Packet format


| Preamble       | Sync word                         | Length | Payload | CRC            |
|----------------|-----------------------------------|--------|---------|----------------|
|0101010101010101|00001010 00000101 01011010 10101010|11100000|xxxxxxxxx|0111011111111111|
|          0x5555|                                   |     0x7|         |                |


### Payload

| ???    | Remote ID       | Group  | Button | Count1 | Count2 |
|--------|-----------------|--------|--------|--------|--------|
|01011010|11101011 00000110|10000000|00010000|11111101|00000110|
|        |         0x60D75A|     0x1|     0x8|    0xBF|    0x60|
