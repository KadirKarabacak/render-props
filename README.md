# **Render Props**

Bir componenti yeniden kullanabilmek için oluşturulan yapıdır. Örneğin bir "List" componentimiz var 👉 <br>

-   **function List ( { render } ) { }** propunu alıyoruz ve bu component içerisinde 👉 **<ul>{displayItems.map(render)}</ul>** şeklinde kullanabiliriz. Daha sonra List componentini her kullandığımızda render propuna verdiğimiz component map methodundan sonra gelen yere yerleşir.
-   render propumuz her zaman bir **fonksiyon** olmalıdır.

# **Higher Order Components**

-   Higher order component basitçe bir fonksiyondur ve bir component döndürür. 3. taraf bir kütüphaneden gelen hazır componentler üzerinde değişiklik yapabilmek için kullanışlıdır.
-   Fonksiyonumuza componentimizi parametre olarak veririz ve fonksiyon içerisinden yeni bir component döndürüp parametre olarak verdiğimiz componentimizi yeni dönecek component içerisinde istediğimiz şekilde kullanabiliriz.

# **Compound Component Pattern**

-   <a href="https://shorturl.at/gr346">Bu linke</a> göz atabilirsin.
-   Compound Component ( Bileşik Bileşen ) bizleri bir component üzerinden çok fazla prop geçirmekten kurtarır ve component içerisindeki değerleri istediğimiz şekilde düzenlememize olanak verir.
-   Aynı componenti bazı kısımları olmadan veya daha fazlasını dahil ederek, tamamen farklı bir stilde kullanabiliriz.
-   State farklı instance'larda tamamen encapsulated (kapsüllenmiştir), birbirinden bağımsız şekilde hareket edebilirler.
-   **Örneğin** 👇
-   <"Counter
    iconIncrease="+"
    iconDecrease="-"
    label="My NOT so flexible counter"
    hideLabel={false}
    hideIncrease={false}
    hideDecrease={false}
    />
-   **Yerine** 👇
-   <"Counter>
    <"Counter.Decrease icon="-" />
    <"Counter.Count />
    <"Counter.Label>My super flexible counter</"Counter.Label>
    <"Counter.Increase icon="+" />
    <"/Counter>
-   İlk olarak bir context oluşturmamız lazım. **const CounterContext = createContext()**
-   İkinci adımımızda bir **parent** component oluşturmalıyız.
-   Üçüncü olarak **child** componentleri oluşturmamız lazım. [ Decrease, Increase ... ]
-   Dördüncü adımda ise **Child componentleri Parent componente** properties olarak eklemeliyiz.
