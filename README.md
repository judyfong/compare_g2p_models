## [cadia-lvl/tts_data](https://github.com/cadia-lvl/tts_data)
#### Type: 
Sequitur model
#### Location: 
available at this directory: pron_data/ipd_clean_slt2018.mdl
#### Dependencies: just do `pip3 install -r requirements`
#### Usage: Look at tests/tests.py as to how to call it.
####  Example 

input file: 
`<phrase>tab<list-name>`
```
Mammon vor er alhreinn orðinn	althingi
forseti	althingi
```

output file:
`<phrase>tab<list-name>tab<phonemes>`
```
Mammon vor er alhreinn orðinn	althingi	~ m a m ɔ n	v ɔː r	ɛ r	aː l̥ r̥ ei t n̥	ɔ r ð ɪ n ~
forseti	althingi	~ f ɔ r̥ s ɛ t ɪ ~
```
