# ImageDataGenerator
<h2></h2>
<p>縦横比が極端に異なる画像データを用いて、機械学習モデルを学習する際に、単純にImageDataGeneratorを用いて行おうとすると、すべての画像に対し同一のリサイズが行われ、その結果、縦横比が極端に異なる画像データは間延びしたような（ぼやけた．歪曲した）画像での学習となってしまう．その結果、機械学習モデルの精度の低下につながる恐れがある．<br></p>
<p>ImageDataGeneratorを改良</p>
<hr>
<h3>utils.py</h3>
<p>主な改良点はutils.load_img関数．ImageDataGenerator.flow_from_directory(self, directory, target_size=(256, 256), ...)などでバッチ全体でサイズを統一して、読み込むが、そのため、縦横比の極端な画像は間延びしたような画像にreshapeされてしまう．load_imgで読み込んだ際に、画像の縦横比が異なる場合は、縦横比が同じになるように0paddingすることで正方形の画像に変形してから、読み込まれるようにしている．</p>
<hr>
<h3>image_data_generator.py</h3>
<hr>
<h3>directory_iterator.py</h3>
<hr>
<h3>iterator.py</h3>
