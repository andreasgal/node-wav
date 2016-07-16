node-wav
========

High performance WAV decoder and encoder. The decoder is up to 750x faster than
the 'wav-decoder' npm module.

In addition, in contrast to 'wav-decoder' the result is returned directly instead
of with a promise.

Usage
-----

    let fs = require('fs');
    let wav = require('node-wav');

    let buffer = fs.readFileSync('file.wav');
    let result = wav.decode(buffer);
    console.log(result.sampleRate);
    console.log(result.channelData); // array of Float32Arrays
