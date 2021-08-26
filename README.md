# dvdrental_odev6
patika.dev dvdrental örnek veri tabanı ile sorgular ödev6

1) film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?
```
SELECT ROUND(AVG(rental_rate),3) FROM film;
```
![1](sorgu_1.jpg)
***
2) film tablosunda bulunan filmlerden kaçtanesi 'C' karekteri ile başlar?
```
SELECT COUNT(*) FROM film
WHERE title LIKE 'C%';
```
![2](sorgu_2.jpg)
***
3) film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?
```
SELECT MAX(length) FROM film
WHERE rental_rate IN (0.99);
```
![3](sorgu_3.jpg)
***
4) film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?
```
SELECT COUNT(DISTINCT replacement_cost) FROM film
WHERE length > 150 ;
```
![4](sorgu_4.jpg)
