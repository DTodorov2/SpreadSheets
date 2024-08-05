# SpreadSheets
Documentation for SpreadSheets 

Проектът “SpreadSheets” работи с файлове, като започва работа с файла след първоначалното му отваряне. Няма как да се работи с програмата преди самото отваряне на файл. Ако даденият файл не съществува, се изкарва съобщение “Such file does not exist!” и се пита за друго име на файл. След отварянето на файл има няколко опции за действия с него (Принтиране, затваряне, запазване, запазване като нов, редактиране на клетка). Няма как да се работи с друг файл, докато имаме вече един отворен. За да бъде някоя стойност в клетка валиден тип данна, то тя трябва да бъде едно от следните неща – число (цяло или дробно), формула или string, като за да бъде даден string валиден, той трябва да започва и да  завършва с кавички. Ако някъде в стринга има “ или \, то трябва преди тях да се сложи \, за да могат да бъдат включени в string-а и той да бъде валиден. 
Пример за валиден стринг: “eX\\amp\”le”, като този string ще се интерпретира като “eX\amp”le”.
Пример за невалиден стринг: “eX\amp”le”.

За да бъде дадена формула коректна, то тя трябва да бъде в следния вид: value operation value…, като между всяка стойност и знак (операция или скоба), трябва да има разстояние, като единствено числата, който имат знак отпред не трябва да съдържат спейс по между им (между знака и самото число).
Пример за валидна формула: = ( R1C2 + R2C2 ) * 3 ^ 2 – ( -2 ).
Пример за невалидна формула: = (-2) * 3^3 + (R1C2+R2C2).

За да бъде едно число валидно, то ако е дробно – трябва да бъде изписано с точка и не трябва да има разстояние между числото и знака пред него.

Функцията “принтиране” изкарва съдържанието на файла на конзолата, като броя на клетките на всеки ред се определя от максималния брой клетки на всички редове. Ако в дадена клетка имаме невалиден тип данна, се проверява за изпусната запетая от потребителя.
Пример: При въведена стойност 123”example”, ще се изведе съобщение, че има изпусната запетая на съотвения ред и колона, на която се намира данната и след кой знак е изпусната запетаята. Това действие бива последвано от въпроса към потребителя „Do you want to continue? – y/n“, като при положителен отговор от страна на потребителя на мястото на невалидната данна се записва Invalid, а при отрицателен – програмата бива спирана.
 
Ако в някоя клетка има формула, то при извеждането на таблицата на екрана се изкарва самата стойност на формулата в клетката. Създава се вектор от всички числа, които участват във формулата и вектор от всички операции, които участват във формулата. След използването на две числа, те се премахват от вектора и самата операция, която използваме, също се премахва от вектора с операции. Формулата трябва да бъде написана в следния вид “= 3 ^ 2 + ( -2 ) * R1C2”, тоест трябва да има space след всеки символ, иначе ще бъде сметната за невалиден тип данна. 
•	Ако в някоя клетка има формула от вида “= 2 / 0”, то в таблицата ще бъде записано “ERROR”, тъй като деленето на нула е неправилно. Същата реакция предизвиква и повдигането на число на негативна степен.
•	Числата могат да се записват както в нормален вид, така и със знаци отпред - примерно “+23”. 

Функцията “Close file” затваря вече отвореният файл, като след това потребителят бива питан дали иска да продължи работата си с програмата, ако не - то програмата спира, иначе се изисква ново име на файл, с който следва да се работи. 

Функцията “Save file” запазва информацията в същия файл, който е вече отворен. 

Функцията “Save file as” запазва информацията в нов файл. Изисква се име на файл, в който да бъде запазена таблицата, като разширението на файла трябва да бъде задължително “.txt”. 

Функцията “Edit cell” променя съдържанието на дадена клетка, като за да се избере точната клетка, то потребителят трябва да въведе номер на колона и след това номер на ред, след което се изисква информацията, с която да бъде заместена досегашната такава. След което се извежда съобщение:  
•	Ако съобщението е от вида “Invalid index!”, то това значи, че не съществува клетка с посочените координати. 
•	Ако съобщението е “ is invalid data type!”, то това означава, че потребителят не е въвел валиден тип данна, след което се извежда описание на валидните типове данни и „Cell edit failed!“.
•	Ако съобщението е “Cell edited successfully!”, то потребителят е направил всичко правилно. 

Функцията “Exit program” спира програмата, като се грижи за затварянето на файла, ако той не е бил затворен досега. 
  

