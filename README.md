This is a java version of Chinese tokenization descried in BERT, including basic tokenization and wordpiece tokenization.

## Motivation

In production, we usually deploy the BERT related model by tensorflow serving for high performance and flexibility. However, our application may not developed by python. Hence, we have to rewrite the tokenization module.

## Usage

Just run `Preprocess.java`, you can get result. Now, it support single and pair sentence both.

Moreover, for Chinese natural language processing, we add **full turn to half angle** and **uppercase to lowercase** operation.

## Reporting issues

Please let me know, if you encounter any problems.

## Updata

修改`BasicTokenizer.java`中，`isPunctuation()`方法，因为这里有判断字符类型，在Python中使用的是`unicodedata.category(char)`，这里使用的是直接判断，但是这里写的不够全面，我在这里补充了一点，让结果与Python版本的tokenizer更加接近一些。
