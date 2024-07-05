# ossify
Ossify is C toolkit to build components of an operating system.

Ossify is based on trace-driven simluation, to allow components of an operating system to be developed and tested without requiring a whole working system and without the pain of hardware bring up.

Components can be over-simplified for pedagogy or for placeholders to allow development to focus on other modules.

The supplied example has highly simplified non-realistic page table and scheduler implementations, to illustrate that it is not necessary to aim for realism to get started.

I use [Pin](https://www.intel.com/content/www/us/en/developer/articles/tool/pin-a-dynamic-binary-instrumentation-tool.html) to generate trace files on an Intel platform; a similar tool on any other arechitecture can be used as long as the traces follow the same format:

`<hex address> <type>`

where `<hex address>` is written in `0xdddddd` format (for any number of digits -- up to the address length) and `<type>` is one of `I` for instruction fetch, `R` for data read, `W` for data write and `X` if you want to fake the effect of an exception, in which case, the hex number is latency of the exception in clock ticks.

## Why Ossify?
Ossify, in English, in one meaning, means to become _rigid or fixed; to cease developing_. That is what far too many operating systems are like, because it's too hard to try out new ideas. Does that have to be true?

## Watch this space: code to follow
