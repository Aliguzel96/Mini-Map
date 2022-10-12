# Mini-Map

## (&#x1F535;) Mini Map üzerinde Kamera Takibi:

1 - Objenin içerisinde bulunan kameranın yanına yeni bir kamera ekledik. Bu kemaranın ayarlarındaki "Projection kısmını -> Orthographic olarak ayarladık.
2 - Sonrasında ana kameranın Deph değerini diğer kameradan daha yüksek bir değere set ediyoruz. (Böylelikle game ekranı buradan görüntülensin)
3 - Bir Canvas oluşturup içerisine bir Image yerleştiriyoruz (mimi Map'in görüneceği yer).
      Bu Image içerisine bir rawImage ekliyoruz.
        Assets kısmında bir "Render Texture" oluşturuyoruz. Oluşturduğumuz bu Texture'ı RawImage'e atıyoruz.
4 - Mini Map'e gelip (Inspector -> Target Texture kısmına oluşturduğumuz Render Texture'ı atıyoruz.
5 - Bu noktada kamerada simgesel olarak görüntüleceğimiz bir Sprite ekliyoruz. (Unity 3D Sprite oluşturmak: Create - GameObject - Go Inspector and add a Sprite Renderer to Components.)
6 - Oluşturduğumuz bu Raw Image'i Ana Kamera ve Mini Kamera içerisine konumlandırıyoruz ve gereken konumlandırmayı yapıyoruz.
7 - Daha sonra bu Raw Image'i ana kameradan çıkartmak, görünürlüğünü kapatmak için bu Raw Image'a bir Layer ekliyoruz. 
Sonrasında ana kameraya gelip Culling Maske ayarından oluşturduğumuz bu Layer'i kaldırıyoruz.
