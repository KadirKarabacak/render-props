# Render Props
Bir componenti yeniden kullanabilmek için oluşturulan yapıdır. Örneğin bir "List" componentimiz var 👉 <br>
* **function List ( { render } ) { }** propunu alıyoruz ve bu component içerisinde 👉 **<ul>{displayItems.map(render)}</ul>** şeklinde kullanabiliriz. Daha sonra List componentini her kullandığımızda render propuna verdiğimiz component map methodundan sonra gelen yere yerleşir
