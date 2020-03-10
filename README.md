# JapaneseNLI
Google Colabで日本語テキスト推論を試す

## 概要
含意関係認識（Recognizing Textual Entailment, RTE）または自然言語推論・テキスト推論(Natural Language Inference)は、以下の例のように、ある前提文に対して仮説文が推論できるか否かを判定する自然言語処理のタスクです。
```
前提文： 太郎は花子が山頂まで登っている間に、山頂まで登った。
仮説文： 太郎は花子が山頂まで登る前に、山頂まで登った。 
正解ラベル： 含意 (entailment)

前提文： 太郎は花子が山頂まで登る前に、山頂まで登った。 
仮説文： 太郎は花子が山頂まで登っている間に、山頂まで登った。
正解ラベル： 非含意 (neutral)

前提文： 太郎は花子が山頂まで登る前に、山頂まで登った。
仮説文： 太郎は花子が山頂まで登った後に、山頂まで登った。 
正解ラベル： 矛盾 (contradiction)
```

[JapaneseBERT_NLI.ipynb](https://github.com/verypluming/JapaneseNLI/blob/master/JapaneseBERT_NLI.ipynb):
[Transformers](https://github.com/huggingface/transformers)ライブラリのBERTとGoogle Colabを用いて日本語テキスト推論を試せるコードです。

[JapaneseXLM_NLI.ipynb](https://github.com/verypluming/JapaneseNLI/blob/master/JapaneseXLM_NLI.ipynb):
[Transformers](https://github.com/huggingface/transformers)ライブラリのXLMとGoogle Colabを用いて日本語テキスト推論を試せるコードです。

## 学習データの用意
ファインチューニング用の学習データがある場合は、一行目はタブ区切りでpremise, hypothesis, gold_labelと記述し、二行目以降にタブ区切りで前提文、仮説文、正解ラベル(entailment, contradiction, neutralの3値)が書かれたtrain.tsvファイルを用意して、[Google Drive](https://www.google.co.jp/drive/apps.html)にアップロードしてください。
[train.tsvのサンプル](https://github.com/verypluming/JapaneseNLI/blob/master/train.tsv)

## Contact
Hitomi Yanaka hitomi.yanaka@riken.jp

## License
Apache License