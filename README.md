## [cadia-lvl/tts_data](https://github.com/cadia-lvl/tts_data)
#### Type: 
Sequitur model
#### Location: 
model available here: [pron_data/ipd_clean_slt2018.mdl](https://github.com/cadia-(vl/tts_data/blob/master/pron_data/ipd_clean_slt2018.mdl)
#### Dependencies: just do `pip3 install -r requirements`
#### Usage: Look at [tests/tests.py](https://github.com/cadia-lvl/tts_data/blob/master/tests/tests.py) as to how to call it.
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
## [rkjaran/g2p-service](https://github.com/rkjaran/g2p-service)
#### Type 
sequitur wrapper
#### Location
doesn't come with a model but there's an endpoint: [https://nlp.talgreinir.is/pron/derp](https://nlp.talgreinir.is/pron/derp)
#### Dependencies
install via dockerfile
#### Usage
#### Example

single word
```
$ curl -XGET https://nlp.talgreinir.is/pron/derp | jq
[
  {
    "results": [
      {
        "posterior": 0.9138450652404999,
        "pronunciation": "t ɛ r̥ p"
      }
    ],
    "word": "derp"
  }
]
```

Multiple word support with a POST.
    
    $ cat <<EOF | curl -XPOST -d@- https://nlp.talgreinir.is/pron | jq
    {"words": ["herp", "derp"]}
    EOF
    [
      {
        "results": [
          {
            "posterior": 0.9251423160703962,
            "pronunciation": "h ɛ r̥ p"
          }
        ],
        "word": "herp"
      },
      {
        "results": [
          {
            "posterior": 0.9138450652404999,
            "pronunciation": "t ɛ r̥ p"
          }
        ],
        "word": "derp"
      }
    ]
    
Append `?t=tsv` to get the response in the Kaldi lexicon format.

`Hasler	1.0	h a s t l ɛ r`

## [grammatek/g2p-thrax](https://github.com/grammatek/g2p-thrax)
#### Type
thrax - rule based
#### Location
need to build it yourself from the repo
#### Dependencies: 
Thrax and OpenFST
#### Usage
TODO
#### Example
TODO
input

output

## [althingi/s5](https://github.com/cadia-lvl/kaldi/tree/master/egs/althingi/s5)
#### Type
sequitur
#### Location
terra:/models/althingi
#### Dependencies: 
sequitur
#### Usage
It's best to use this only for ASR, not TTS because it's not precise enough.
TODO
#### Example
TODO
input
```
local/
output


## repo link
#### Type
#### Location
#### Dependencies:
#### Usage
#### Example

input

output
