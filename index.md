# End-to-end Text-to-speech for Low-resource Languages by Cross-Lingual Transfer Learning

**Paper:** [arXiv]()

**Authors:** Yuan-Jui Chen\*, Tao Tu\*, Cheng-chieh Yeh, Hung-yi Lee

**Abstract:** End-to-end text-to-speech (TTS) has shown great success on large quantities of paired text plus speech data. However, laborious data collection remains difficult for at least 95\% of the languages over the world, which hinders the development of TTS in different languages. In this paper, we aim to build TTS systems for such low-resource (target) languages where only very limited paired data are available. We show such TTS can be effectively constructed by transferring knowledge from a high-resource (source) language. Since the model trained on source language cannot be directly applied to target language due to input space mismatch, we propose a method to learn a mapping between source and target linguistic symbols. Benefiting from this learned mapping, pronunciation information can be preserved throughout the transferring procedure. Preliminary experiments show that we only need around 15 minutes of paired data to obtain a relatively good TTS system. Furthermore, analytic studies demonstrated that the automatically discovered mapping correlate well with the phonetic expertise.

All phrases below are unseen during training.
Since our goal is to investigate transfer learning for languages with small amounts of data, all audios on this demo page were synthesized using Griffin-Lim for faster experiment cycle as stated in the paper. 

Contents

* [Samples for each target language with small amounts of data](#head1)
    * [Mandarin (phn2phn)](#head1-zh-phn2phn)
    * [French (phn2phn)](#head1-fr-phn2phn)
    * [French (phn2char)](#head1-fr-phn2char)
    * [German (phn2phn)](#head1-de-phn2phn)
    * [German (phn2char)](#head1-de-phn2char)
* [Symbol Mapping](#head2)
    * [Mandarin](#head2-zh)
    * [French](#head2-fr)
    * [German](#head2-de)

## <a name="head1"></a>Samples for each target languages with small amount of data
These samples refer to Section 4.3 of our paper. Here we demonstrate the performance of our 3 transfer learning methods on three languages : Mandarin, German and French.


### <a name="head1-zh-phn2phn"></a>Mandarin (phn2phn)

Amount | Text | Unified | Learned | Separate | Scratch |
-------|:----:|:-------:|:-------:|:--------:|:-------:|
25 min | 還能笑得這<br>麼開心 | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0428_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0428_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0428_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0428_scratch.wav" type="audio/wav"></audio> |
25 min | 想在這樣的<br>楓紅裡野餐 | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0203_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0203_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0203_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/25min_all/f05-read-0203_scratch.wav" type="audio/wav"></audio> |
15 min | 祝你快快寫<br>出好玩的新<br>遊戲 | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0028_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0028_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0028_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0028_scratch.wav" type="audio/wav"></audio> |
15 min | 原來我們只<br>差一天 | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0728_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0728_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0728_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/15min_all/f05-read-0728_scratch.wav" type="audio/wav"></audio> |


Method | Text | 30 min | 25 min | 20min | 15min |
-------|:----:|:------:|:------:|:-----:|:-----:|
Unified | 就原諒我這<br>個虛榮的願<br>望吧 | <audio controls=""><source src="demo/mandarin/share_all/f05-read-0372_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/share_all/f05-read-0372_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/share_all/f05-read-0372_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/share_all/f05-read-0372_15min.wav" type="audio/wav"></audio> |
Learned | 就要在大阪<br>多待一天了 | <audio controls=""><source src="demo/mandarin/map_all/f05-read-0065_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/map_all/f05-read-0065_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/map_all/f05-read-0065_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/map_all/f05-read-0065_15min.wav" type="audio/wav"></audio> |
Separate | 好像輕輕嘆<br>口氣 | <audio controls=""><source src="demo/mandarin/separate_all/f05-read-0044_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/separate_all/f05-read-0044_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/separate_all/f05-read-0044_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/mandarin/separate_all/f05-read-0044_15min.wav" type="audio/wav"></audio> |



### <a name="head1-fr-phn2phn"></a>French (phn2phn)

Amount | Text | Unified | Learned | Separate | Scratch |
-------|:----:|:-------:|:-------:|:--------:|:-------:|
15 min | le conseil supérieur<br>de la magistrature<br>est composé de<br>cinq membres titulaires | <audio controls=""><source src="demo/french/phn2phn/15min_all/49_predicted_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/15min_all/49_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/15min_all/49_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/15min_all/49_predicted_scratch.wav" type="audio/wav"></audio> |
15 min | votre dossier de<br>candidature doit être<br>accompagné des éléments<br>suivants | <audio controls=""><source src="demo/french/phn2phn/15min_all/87_predicted_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/15min_all/87_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/15min_all/87_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/15min_all/87_predicted_scratch.wav" type="audio/wav"></audio> |
10 min | il est moins<br>souvent utile de<br>savoir si la<br>réponse est exacte<br>ou erronée | <audio controls=""><source src="demo/french/phn2phn/10min_all/20_predicted_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/10min_all/20_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/10min_all/20_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/10min_all/20_predicted_scratch.wav" type="audio/wav"></audio> |
10 min | c'est dans ces<br>centres sociaux non<br>spécialisés en<br>toxicomanie| <audio controls=""><source src="demo/french/phn2phn/10min_all/11_predicted_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/10min_all/11_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/10min_all/11_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/10min_all/11_predicted_scratch.wav" type="audio/wav"></audio> |


Method | Text | 15 min | 12.5 min | 10min |
-------|:----:|:------:|:------:|:-----:|
Unified | elle ne sent<br>que par sa tête | <audio controls=""><source src="demo/french/phn2phn/share_all/44_predicted_15min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/share_all/44_predicted_12_5min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/share_all/44_predicted_10min.wav" type="audio/wav"></audio> |
Learned | tous les animaux<br>vivent en accord<br>avec leur espèce |<audio controls=""><source src="demo/french/phn2phn/mapping_all/6_predicted_15min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/mapping_all/6_predicted_12_5min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/mapping_all/6_predicted_10min.wav" type="audio/wav"></audio> |
Separate | elle est constituée<br>de la liste des<br>titres | <audio controls=""><source src="demo/french/phn2phn/separate_all/10_predicted_15min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/separate_all/10_predicted_12_5min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2phn/separate_all/10_predicted_10min.wav" type="audio/wav"></audio> |

### <a name="head1-fr-phn2char"></a>French (phn2char)

Amount | Text | Learned | Separate | Scratch |
-------|:----:|:-------:|:-------:|:--------:|
15 min | il est alors<br>utile de poursuivre<br>les conseils diététiques<br>précédents | <audio controls=""><source src="demo/french/phn2char/15min_all/43_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/15min_all/43_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/15min_all/43_predicted_scratch.wav" type="audio/wav"></audio> |
15 min | les agents peuvent<br>communiquer coopérer | <audio controls=""><source src="demo/french/phn2char/15min_all/84_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/15min_all/84_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/15min_all/84_predicted_scratch.wav" type="audio/wav"></audio> |
10 min | il ne faut pas<br>aller trop vite | <audio controls=""><source src="demo/french/phn2char/10min_all/7_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/10min_all/7_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/10min_all/7_predicted_scratch.wav" type="audio/wav"></audio> |
10 min | les cercles de<br>couleurs transparentes ne<br>se superposent que<br>partiellement | <audio controls=""><source src="demo/french/phn2char/10min_all/12_predicted_mapping.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/10min_all/12_predicted_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/10min_all/12_predicted_scratch.wav" type="audio/wav"></audio> |

Method | Text | 15 min | 12.5 min | 10min |
-------|:----:|:------:|:------:|:-----:|
Learned | il est moins<br>souvent utile de<br>savoir si la<br>réponse est exacte<br>ou erronée | <audio controls=""><source src="demo/french/phn2char/mapping_all/20_predicted_15min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/mapping_all/20_predicted_12_5min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/mapping_all/20_predicted_10min.wav" type="audio/wav"></audio> |
Separate | elle est constituée<br>de la liste des titres | <audio controls=""><source src="demo/french/phn2char/separate_all/10_predicted_15min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/separate_all/10_predicted_12_5min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/french/phn2char/separate_all/10_predicted_10min.wav" type="audio/wav"></audio> |



### <a name="head1-de-phn2phn"></a>German (phn2phn)

Amount | Text | Unified | Learned | Separate | Scratch |
-------|:----:|:-------:|:-------:|:--------:|:-------:|
25 min | Sie hatte zwei<br>Töchter die längst<br>verheiratet waren | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_01_f000014_0_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_01_f000014_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_01_f000014_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_01_f000014_0_scratch.wav" type="audio/wav"></audio> |
25 min | Wohin sie führen<br>fragte ich Sie<br>lachte und sagte<br>Weiter | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_04_f000032_0_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_04_f000032_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_04_f000032_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/25min_all/werde_die_du_bist_04_f000032_0_scratch.wav" type="audio/wav"></audio> |
15 min | Ich wurde gestraft<br>und erfuhr daß<br>ich etwas sehr<br>Böses getan hatte | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_02_f000049_0_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_02_f000049_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_02_f000049_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_02_f000049_0_scratch.wav" type="audio/wav"></audio> |
15 min | Er grüßte blieb<br>stehen er wollte<br>mich ansprechen | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_08_f000082_0_share.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_08_f000082_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_08_f000082_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/15min_all/werde_die_du_bist_08_f000082_0_scratch.wav" type="audio/wav"></audio> |


Method | Text | 30 min | 25 min | 20min | 15min |
-------|:----:|:------:|:------:|:-----:|:-----:|
Unified | An den Fenstern weiße<br>Gardinen und braune<br>Kinderköpfchen die<br>lustig herauslugten | <audio controls=""><source src="demo/german/phn2phn/share_all/werde_die_du_bist_04_f000029_0_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/share_all/werde_die_du_bist_04_f000029_0_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/share_all/werde_die_du_bist_04_f000029_0_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/share_all/werde_die_du_bist_04_f000029_0_15min.wav" type="audio/wav"></audio> |
Learned | Ich habe ja noch<br>beinahe ein halbes<br>Jahrhundert vor mir | <audio controls=""><source src="demo/german/phn2phn/map_all/werde_die_du_bist_05_f000082_0_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/map_all/werde_die_du_bist_05_f000082_0_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/map_all/werde_die_du_bist_05_f000082_0_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/map_all/werde_die_du_bist_05_f000082_0_15min.wav" type="audio/wav"></audio> |
Separate | Was die Andern<br>taten das war<br>für sie das Richtige | <audio controls=""><source src="demo/german/phn2phn/separate_all/werde_die_du_bist_02_f000055_0_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/separate_all/werde_die_du_bist_02_f000055_0_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/separate_all/werde_die_du_bist_02_f000055_0_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2phn/separate_all/werde_die_du_bist_02_f000055_0_15min.wav" type="audio/wav"></audio> |

### <a name="head1-de-phn2char"></a>German (phn2char)

Amount | Text | Learned | Separate | Scratch |
-------|:----:|:-------:|:-------:|:--------:|
25 min | Nun aber sind<br>mir fast seine<br>Gesichtszüge entschwunden | <audio controls=""><source src="demo/german/phn2char/25min_all/werde_die_du_bist_02_f000174_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/25min_all/werde_die_du_bist_02_f000174_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/25min_all/werde_die_du_bist_02_f000174_0_scratch.wav" type="audio/wav"></audio> |
25 min | Ich saß stundenlang<br>und tat nichts und<br>dämmerte so hin | <audio controls=""><source src="demo/german/phn2char/25min_all/werde_die_du_bist_02_f000141_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/25min_all/werde_die_du_bist_02_f000141_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/25min_all/werde_die_du_bist_02_f000141_0_scratch.wav" type="audio/wav"></audio> |
15 min | Von einer Reise zu<br>meinen Töchtern konnte<br>keine Rede sein | <audio controls=""><source src="demo/german/phn2char/15min_all/werde_die_du_bist_02_f000127_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/15min_all/werde_die_du_bist_02_f000127_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/15min_all/werde_die_du_bist_02_f000127_0_scratch.wav" type="audio/wav"></audio> |
15 min | Ich tat was ich<br>konnte es war<br>auch wirklich nicht<br>zu viel | <audio controls=""><source src="demo/german/phn2char/15min_all/werde_die_du_bist_02_f000089_0_map.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/15min_all/werde_die_du_bist_02_f000089_0_separate.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/15min_all/werde_die_du_bist_02_f000089_0_scratch.wav" type="audio/wav"></audio> |

Method | Text | 30 min | 25 min | 20min | 15min |
-------|:----:|:------:|:------:|:-----:|:-----:|
Learned | Ich hatte solche<br>Unlust zu meinen<br>Töchtern zu reisen | <audio controls=""><source src="demo/german/phn2char/map_all/werde_die_du_bist_02_f000143_0_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/map_all/werde_die_du_bist_02_f000143_0_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/map_all/werde_die_du_bist_02_f000143_0_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/map_all/werde_die_du_bist_02_f000143_0_15min.wav" type="audio/wav"></audio> |
Separate | Immer nur wandle<br>ich am Strand<br>entlang weiter und<br>weiter | <audio controls=""><source src="demo/german/phn2char/separate_all/werde_die_du_bist_05_f000072_0_30min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/separate_all/werde_die_du_bist_05_f000072_0_25min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/separate_all/werde_die_du_bist_05_f000072_0_20min.wav" type="audio/wav"></audio> | <audio controls=""><source src="demo/german/phn2char/separate_all/werde_die_du_bist_05_f000072_0_15min.wav" type="audio/wav"></audio> |






## <a name="head2"></a>Symbol Mapping
The mappings in the following derive from 15 minutes target paired-data.
For a better presentation and comparison, we mapped all the phonemes to IPA.


### <a name="head2-zh"></a>Mandarin-ZH (phn2phn)

Phoneme (EN)  | Phoneme (ZH) | | Phoneme (EN) | Phoneme (ZH)
--------------|--------------|-|--------------|--------------
n | n | | ʃ | ʂ
e | e | | b | p
d | t | | ɡ | k
z | ɕ | | s | s
æ | a | | f | f
w | w | | i | i
ɑ | ɑ | | m | m
h | h | | ə | ə
j | j


- - - 

### <a name="head2-de"></a>German (phn2char)

Phoneme (EN) | Character (DE)| | Phoneme (EN) | Character (DE)
--------------|--------------|-|--------------|--------------
ŋ | n | | z | s
a | e | | p | p
t | t | | ʃ | c
ɡ | g | | d | d
b | b | | ɔ | o
k | k | | v | w
ʊ | u | | ɪ | i
ɑ | a | | æ | ä
m | m | | h | h
j | j | | ɫ | l
f | f


### <a name="head2-fr"></a>French (phn2char)

Phoneme (EN) | Character (FR)| | Phoneme (EN) | Character (FR)
--------------|--------------|-|--------------|--------------
n | n | | ɑ | a
p | p | | t | t
k | c | | ɡ | g
z | s | | d | d
b | b | | v | v
w | o | | ɝ | e
m | m | | i | i
h | r | | f | f
