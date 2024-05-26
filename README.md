Магдалена Трајковска 223156

1. **Control Flow Graph**


![Untitled Diagram drawio (2)](https://github.com/magdalenatrajkovska/SI_2024_lab2_223156/assets/139167699/4c52a532-0a11-449b-82f4-71368c4a1031)



2. **Цикломатска комплексност**

Цикломатската комплексност на овој код е 10, истата ја добив преку формулата P+1, каде што P е бројот на предикатни јазли. Во случајoв P=9 {има 9 if и for јазли}, па цикломатската комплексност изнесува 10.

3. **Тест случаи според критериумот Every Branch**
   ![image](https://github.com/magdalenatrajkovska/SI_2024_lab2_223156/assets/139167699/1443e46f-bf76-4e72-919b-4137d12aa163)


4. **Тест случаи според критериумот Multiple Condition**
   ![image](https://github.com/magdalenatrajkovska/SI_2024_lab2_223156/assets/139167699/a061d389-a01c-4b6c-8ac5-5a13208121b0)


5. **Објаснување на напишаните unit tests**
   -every branch
 1)  allItems = null
    фрлa RuntimeException("allItems list can't be null!")
   
 2)  "allItems=[Item(null, ""1111"", 300, 0.50),
                  Item(""Item2"", ""2222"", 350, -1)]
payment=10000;"
  2 објекти, програмата заврсшува true

3)"allItems=[Item(null, ""2222"", 350, 0.500),
                  Item(""Item2"", ""666"", 350, -1)]
payment=10;"
 2 објекти и голема вредност за payment, програмата заврсшува false

 4) "allItems=[Item("""", ""hhhh"", 100, -1),          
    payment=100;"
not valid Barcode-> фрла RuntimeException("Invalid character in item barcode!")

6) "allItems=[Item(null, null , 100, -1),                
payment=100;"
null Barcode и Name -> фрлa RuntimeException("No barcode!")


   -multiple condition
1) allItems = [Item(Name = 012, Barcode = 000l, Price = 355, Discount = 0.5)], payment = 145
   TTT - сите се труе и програмата продолжува во if
2) allItems = [Item(Name = 012, Barcode = 125, Price = 355, Discount = -1)], payment = 146
   TFF -   програмата нема да продолжи во if
3)	allItems = [Item(Name = 012, Barcode = 125, Price = 355, Discount = 0.5)], payment = 147
   TTF -   програмата нема да продолжи во if
4)	allItems = [Item(Name = 012, Barcode = 125, Price = 200, Discount = -1)], payment = 148
   FXX -   програмата нема да продолжи во if 				

		




				


   
   
