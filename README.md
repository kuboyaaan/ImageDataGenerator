# ImageDataGenerator
<h2></h2>
<p>縦横比が極端に異なる画像データを用いて、機械学習モデルを学習する際に、単純にImageDataGeneratorを用いて行おうとすると、すべての画像に対し同一のリサイズが行われ、その結果、縦横比が極端に異なる画像データは間延びしたような（ぼやけた．歪曲した）画像での学習となってしまう．その結果、機械学習モデルの精度の低下につながる恐れがある．<br></p>
<p>ImageDataGeneratorを改良</p>
<hr>
<h3>utils.py</h3>
<hr>
<h3>image_data_generator.py</h3>
<hr>
<h3>directory_iterator.py</h3>
<hr>
<h3>iterator.py</h3>
