## Table of Contents
* [cadia-lvl/tts-data](#cadia-lvltts_data)
* [atliSig/g2p](#atlisigg2p)
* [rkjaran/g2p-service](#rkjarang2p-service)
* [grammatek/g2p-thrax](#grammatekg2p-thrax)
* [althingi/s5](#althingis5)

## [cadia-lvl/tts_data](https://github.com/cadia-lvl/tts_data)
#### Type: 
Sequitur model
#### Location: 
model available here: [pron_data/ipd_clean_slt2018.mdl](https://github.com/cadia-lvl/tts_data/blob/master/pron_data/ipd_clean_slt2018.mdl)
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


## [atliSig/g2p](https://github.com/atliSig/g2p)
This model was used for creating tts data collection scripts and for training unit selection voices by LVL.
#### Type
Sequitur model
#### Location
[https://github.com/atliSig/g2p/blob/master/data/ipd_clean_slt2018.mdl](https://github.com/atliSig/g2p/blob/master/data/ipd_clean_slt2018.mdl)
#### Dependencies:
they're all listed in [requirements.txt](https://github.com/atliSig/g2p/blob/master/requirements.txt) within the repo
#### Usage
```
    Input arguments:
    * src_path (str): The path to the file containing multiple
    utterances, one per line
    * out_path (str): The target path the the file that stores
    the results.
    * n_jobs (int): The maximum number of processes that can
    be used to execute the given calls.
    * contains_scores (bool): If True, each line in the input file
    is e.g. <sentence>\t<source_id>\t<score> else it is
    <sentence>\t<source_id>
    * translator_options (Options instance): Options passed onto g2p.Translator
```
#### Example

input - tsv file
```
Ég held að það sé ekki rétt orð, þetta komi ekkert almanakinu við.
Fréttirnar eru sko aldeilis dæmalausar.
Það var miði í póstkassanum.
Hann glennti fætur hennar í sundur og reyndi að þrengja sér inn í hárlaust skaut hennar.
Ég tel að þetta sé óskaplega mikil sóun á mannauði hjá einni þjóð.
Yfirverkfræðingur hjá Reykjavíkurborg segir að sökin liggi hjá ökumönnum.
Og nú átti sem sagt að hafa sama háttinn á gagnvart stúdentum hér við Háskólann.
Bæði almennt og sérstakt veiðigjald er lagt flatt sem föst krónutala á þorskígildiskíló.
Lesendur þurfa að fá tækifæri til að njóta hans.
```

output - tsv file

```
Ég held að það sé ekki rétt orð, þetta komi ekkert almanakinu við.	~ j ɛː ɣ	h ɛ l t	aː ð	θ aː ð	s j ɛː	ɛ h c ɪ	r j ɛ h t	ɔ r ð	θ ɛ h t a	kʰ ɔː m ɪ	ɛ h c ɛ r̥ t	a l m a n aː c ɪ n ʏ	v ɪː ð ~
Fréttirnar eru sko aldeilis dæmalausar.	~ f r j ɛ h t ɪ t n a r	ɛː r ʏ	s k ɔ	a l t ei l ɪ s	t aiː m a l œyː s a r ~
Það var miði í póstkassanum.	~ θ aː ð	v aː r	m ɪː ð ɪ	iː	pʰ ou s t k a s a n ʏ m ~
Hann glennti fætur hennar í sundur og reyndi að þrengja sér inn í hárlaust skaut hennar.	~ h a n	k l ɛ n̥ t ɪ	f aiː t ʏ r	h ɛ n a r	iː	s ʏ n t ʏ r	ɔː ɣ	r ei n t ɪ	aː ð	θ r ei ɲ c a	s j ɛː r	ɪ n	iː	h au r l œy s t	s k œyː t	h ɛ n a r ~
Ég tel að þetta sé óskaplega mikil sóun á mannauði hjá einni þjóð.	~ j ɛː ɣ	tʰ ɛː l	aː ð	θ ɛ h t a	s j ɛː	ouː s k a p l ɛ ɣ a	m ɪː c ɪ l	s ouː ʏ n	auː	m a n œy ð ɪ	ç au	ei t n ɪ	θ j ouː ð ~
Yfirverkfræðingur hjá Reykjavíkurborg segir að sökin liggi hjá ökumönnum.	~ ɪː v ɪ r v ɛ r̥ k f r ai ð i ŋ k ʏ r	ç au	r eiː c a v iː k ʏ r p ɔ r k	s ei j ɪ r	aː ð	s œː c ɪ n	l ɪ c ɪ	ç au	œː k ʏ m œ n ʏ m ~
Og nú átti sem sagt að hafa sama háttinn á gagnvart stúdentum hér við Háskólann.	~ ɔː ɣ	n uː	au h t ɪ	s ɛː m	s a x t	aː ð	h aː v a	s aː m a	h au h t ɪ n	auː	k a k v a r̥ t	s t uː t ɛ n̥ t ʏ m	ç ɛː r	v ɪː ð	h auː s k ou l a n ~
Bæði almennt og sérstakt veiðigjald er lagt flatt sem föst krónutala á þorskígildiskíló.	~ p aiː ð ɪ	a l m ɛ n̥ t	ɔː ɣ	s j ɛ r̥ s t a x t	v eiː ð ɪ c a l t	ɛ r	l a x t	f l a h t	s ɛː m	f œ s t	kʰ r ouː n ʏ tʰ aː l a	auː	θ ɔ r̥ s c i c ɪ l t ɪ s c i l ou ~
Lesendur þurfa að fá tækifæri til að njóta hans.	~ l ɛː s ɛ n t ʏ r	θ ʏ r v a	aː ð	f auː	tʰ aiː c ɪ f aiː r ɪ	tʰ ɪː l	aː ð	n j ouː t a	h a n s ~
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
TODO file io
#### Example
If you are doing this from the project root directory,
```
$./build/thraxg2p --far=grammars/g2p.far
Input string: orð
Output string:  O r D
```

You can also pipe it in through stdin.

## [althingi/s5](https://github.com/cadia-lvl/kaldi/tree/master/egs/althingi/s5)
#### Type
sequitur
#### Location
terra:/models/althingi
#### Dependencies: 
sequitur-g2p
#### Usage
It's best to use this only for ASR, not TTS because it's not precise enough.

train a g2p model with [local/train_g2p.sh](https://github.com/cadia-lvl/kaldi/blob/master/egs/althingi/s5/local/train_g2p.sh)

transcribe words with [local/transcribe_g2p.sh](https://github.com/cadia-lvl/kaldi/blob/master/egs/althingi/s5/local/transcribe_g2p.sh)
#### Example
transcribing words
```
$ srun ./local/transcribe_g2p.sh /models/g2p/sequitur/althingi/g2p.mdl temp/g2p_words.txt
derp	t ɛː r p
orð	ɔ r ð
stack usage:  200

```


## repo link
#### Type
#### Location
#### Dependencies:
#### Usage
#### Example

input

output
