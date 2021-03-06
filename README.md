# Втора лабораториска вежба по Софтверско инженерство
Ванеса Михаилова, бр. на индекс 151133

# Група на код:
Ја добив групата на код 2

# Control Flow Graph
![alt text](https://github.com/vmihailova/SI_Lab2_151133/blob/master/151133_Control_Flow.png?raw=true)

# Цикломатска комплексност
Цикломатската комплексност на овој код е 8, истата ја добив со користење на 3-те формули за одредување на комплексноста.

1. Преку бројот на региони
   V(G) = 8
   
2. Со помош на формулата V(G) = E - N + 2, каде E го претставува вкупниот број на врски помеѓу јазлите, додека N е бројот на јазли.     
   Според горе наведениот граф ги имаме следните податоци:
   - E: 23
   - N: 17   
   V(G) = E - N + 2 = 23 - 17 + 2 = 8

3. Преку формулата P + 1, каде што P е бројот на предикатни јазли. Во овој случај имаме 7 предикатни јазли, со што следува
   V(G) = P + 1 = 7 + 1 = 8


# Тест случаи според критериумот Multiple condtition

Во овој код, според Multiple condition критериумот, ги имаме следниве тест случаеви:

 1. if (user==null) 
    Во овој чекор проверуваме дали внесениот user објект е валиден, поточно дали воопшто имаме user објект. 
    За овој тест случај имаме 2 можни тестови, односно кога имаме user објект и кога немаме
     - Ако имаме внесено user објект, тогаш кодот продолжува да се извршува
     - Ако немаме внесено user објект, односно тој е празен, во тој случај ќе се фрли исклучок, со што завршува кодот
     
    ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/MultipleConditionsDATA/MC1.png?raw=true)
    
 
 2. if (user.getUsername()==null || allUsers.contains(user.getUsername()))
    Во овој чекор проверуваме дали внесениот user објект содржи корисничко име или дали овој корисник постои во листата со сите корисници.
    Овде имаме 3 тестови:
    - Доколку корисникот нема корисничко име, ќе се фрли исклучок, со што завршува кодот и нема да се провери вториот услов
    - Ако корисникот има корисничко име и го има во листата на корисници, повторно ќе се фрли исклучок, со што завршува кодот
    - Ако корисникот има корисничко име и го нема корисникот во листата на корисници, тогаш продолжува да се извршува кодот.
    
    ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/MultipleConditionsDATA/MC2.png?raw=true)
    
 
 3.  if (user.getEmail()==null)
     Во овој чекор проверуваме дали user објектот содржи информација за електронската пошта на корисникот. 
     Овде имаме 2 можни тестови:
      - Доколку имаме вредност за електронската пошта, тогаш кодот продолжува да се извршува
      - Доколку немаме вредност за електронската пошта, ќе се фрли исклучок, со што завршува кодот
     
     ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/MultipleConditionsDATA/MC3.png?raw=true)

 4. if (user.getEmail().charAt(i)=='@')
    Во овој дел од кодот започнуваме со валидацијата на поштенската адреса којашто ја содржи user објектот. Овде го проверуваме дали i-тиот карактер на електронската пошта е '@', поточно се валидира дали некаде во внесената вредност за електронска пошта го имаме @ карактерот.
    Овде имаме 2 можни тестови:
     - Доколку моменталниот карактер е @, тогаш вредноста на atChar променливата ќе се промени во true
     - Доколку моменталниот карактер не е @, тогаш ќе заврши if-от
     
    ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/MultipleConditionsDATA/MC4.png?raw=true)
 
 5. if (atChar && user.getEmail().charAt(i)=='.')
    Во овој дел од валидацијата на електронската пошта, проверуваме доколку претходно е пронајден карактер '@', дали i-тиот карактер е '.'
    Овде имаме 3 можни тестови:
      -  Доколку сеуште не е пронајде @ карактерот, вториот услов нема да се изврши и ќе заврши if-от
      -  Доколку е пронајден @ карактерот, а моменталниот карактер не е . повторно ќе заврши if-от
      -  Доколку е пронајден @ карактерот и моменталниот карактер е . ќе влезе во if-от и вредноста на dotChar ќе ја добие вредноста true
      
    ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/MultipleConditionsDATA/MC5.png?raw=true)
 
 6. if (!atChar || !dotChar)
    Во овој дел од кодот ја правеме главната проверка, поточно проверуваме дали во текот на извршувањето на кодот се пронајдени '@' и '.' карактерите во електронската пошта на корисникот. 
    Разликуваме 3 тестови:
    - Доколку не е пронајден '@' карактерот, вториот услов нема да се провери, кодот влегува во if-от и функцијата враќа false, со што завршува кодот
    - Доколку е пронајден '@' карактерот, ќе се провери и вториот услов, односно дали е пронајден '.' карактерот. Доколку не е пронајден, кодот влегува во if-от и функцијата враќа false, со што завршува кодот
    - Доколку е пронајден '@' карактерот, ќе се провери и вториот услов, односно дали е пронајден '.' карактерот. Доколку е пронајден, кодот не влегува во if-от
    
    ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/MultipleConditionsDATA/MC6.png?raw=true)

# Тест случаи според критериумот Every path

  Според овој критериум, потребно е дефинираме тестови преку кои ќе ги изминеме сите можни патеки, па така од вкупниот број на патеки, имаме 14 возможни, а тоа се следниве:
  
  ![alt text](https://github.com/vmihailova/SI_lab2_151133/blob/master/every_path_criteria.png?raw=true)


# Објаснување на напишаните unit tests
... ...
