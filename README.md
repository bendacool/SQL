### Veri tabanı yönetim sistemleri avantajları 
- Veri tekrarını engeller (data Redundancy)
- Veri tutarlılığı (data consistency)
- Veri paylaşımı / eş zamanlılık (data concurrency)
- Veri güvenliği (data security)
- Veri bütünlüğü (data integrity)
- Veri bağımsızlığı (data independence)
#### Veri tabanı yönetim sistemleri dezavantajları : 
- Vt sisteminin kurulumu ve bakımı klasik dosya sistemine göre daha maliyetli olabilir. 

## SEÇME (SELECTION) İŞLEMİ
![[Pasted image 20241023175034.png]]

![[Pasted image 20241023180352.png]]

![[Pasted image 20241023180436.png]]

![[Pasted image 20241023180803.png]]

![[Pasted image 20241023180824.png]]

![[Pasted image 20241023181938.png]]

![[Pasted image 20241023181958.png]]

![[Pasted image 20241023182117.png]]

## MS SQL SYNTAX

```
CREATE TABLE tablo ( id INT IDENTITY(1,1) PRIMARY KEY,```
```
-- AUTO_INCREMENT yerine IDENTITY kullanılır. 
```
ad VARCHAR(50) NOT NULL, soyad VARCHAR(50), araba INT UNIQUE
```
-- 'UNIQUE' doğrudan sütun tanımının ardından kullanılır. 
```
maas DECIMAL(7,2) DEFAULT 1000,
```
-- DEFAULT değeri MS SQL'de de aynı şekilde tanımlanır.
```
CONSTRAINT FK_araba FOREIGN KEY (araba) REFERENCES arabalar(id));
```
-- Yabancı anahtar tanımlaması.


- **MySQL**: `AUTO_INCREMENT` kullanılır.
- **MSSQL**: `IDENTITY(1,1)` kullanılır. Burada ilk `1` başlangıç değeri, ikinci `1` artış miktarını ifade eder.

- MySQL: `id INT AUTO_INCREMENT PRIMARY KEY`
- MSSQL: `id INT IDENTITY(1,1) PRIMARY KEY`

- **MySQL**: `LIMIT` ifadesi kullanılır.
- **MSSQL**: `TOP` ifadesi kullanılır.

- MySQL: `SELECT * FROM tablo LIMIT 10;`
- MSSQL: `SELECT TOP 10 * FROM tablo;`

- **MySQL**: String birleştirme için `CONCAT()` kullanılır.
- **MSSQL**: String birleştirme için `+` operatörü kullanılır.

- **MySQL**: Bazı veri tipleri MSSQL ile aynı olsa da bazı farklar vardır.
    - Örneğin, `TINYINT`, `TEXT`, `ENUM`, `SET` gibi veri tipleri MySQL'de mevcuttur.
- **MSSQL**: MSSQL'de bu veri tipleri yoktur, ama eşdeğer veri tipleri bulunur.
    - Örneğin, `TINYINT` yerine `SMALLINT`, `TEXT` yerine `VARCHAR(MAX)` kullanılabilir.

- **MySQL**: `BOOLEAN` veri tipi vardır, ama aslında `TINYINT(1)` olarak işlenir.
- **MSSQL**: Doğrudan `BOOLEAN` yoktur, bunun yerine `BIT` kullanılır. `BIT`, 0 veya 1 değerlerini alır.

- **MySQL**: `FOREIGN KEY` tanımı genellikle sütun tanımı içinde yapılır, ancak ayrı bir ifade ile de tanımlanabilir.
- **MSSQL**: `FOREIGN KEY` tanımı için genellikle ayrı bir kısıtlama (constraint) tanımlaması kullanılır.

![[Pasted image 20241023184105.png]]

![[Pasted image 20241023184051.png]]

![[Pasted image 20241023184032.png]]

![[Pasted image 20241023184017.png]]

__`DELETE FROM [TABLE] WHERE [STATEMENT]`__

- ms sql'de daha çok and or kullanılır.

__`UPDATE [TABLE] SET [NEW_DATA] WHERE [STATEMENTS]`__

__``FLOOR(), CEILING(), ROUND()``__ : Bu fonksiyonlar yuvarlama fonksıyonlarıdır.

![[Pasted image 20241023184815.png]]

![[Pasted image 20241023184917.png]]

