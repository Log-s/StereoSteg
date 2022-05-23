# StereoSteg
This tools can encode and decode a text inside a wave side, by using the left and right audio channels.

## Installation

The only python library you need is the wave library.
```bash
pip3 install wave
```

## Usage
### Encode
```bash
python3 stereoSteg_encode.py one_channeled_input.wav two_channaled_output.wav data_to_encode
```
Encoding can take up to a few minutes depending on the input file's size.

### Decode
```bash
python3 stereoSteg_decode.py two_channaled_input.wav
```

## Example

```
╭─log_s@precision ~ ‹main●› 
╰─$ python3 stereoSteg_encode.py original.wav getRickrolled.wav Hero{l3f7_r1gh7_l3f7_r1gh7_1_4m_d1zZy}                                              1 ↵
[+] Configuring output file getRickrolled.wav
[+] Loading input file in memory and trimming
[+] Encoding 304 bits into 9376472 frames
[+] Encoding complete
╭─log_s@precision ~ ‹main●› 
╰─$ python3 stereoSteg_decode.py getRickrolled.wav                                                    
[+] Reading 9376272 frames and ordering by channel
[+] Attempting to detect smallest chunk to assign bit size
[+] Decoding text
[+] Decoded text: Hero{l3f7_r1gh7_l3f7_r1gh7_1_4m_d1zZy}
```
