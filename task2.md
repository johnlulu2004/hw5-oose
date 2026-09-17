# 1. 

This design adheres to Dependency Inversion Principle as Client depends on the FormatUtility abstraction, not on the concrete PDFUtility class.

This design adheres to the Open/Closed principle as new format classes could implement FormatUtility and be added without modifying Client.

This design adheres to the Single Responsibility Principle as the classes only have one responsibility. PDFUtility is only responsible for formatting into PDF; TaxReport is only responsible for supplying the raw data.

This design adheres to the Interface Segregation Principle as FormatUtility only defines one focused method, which allows it to stay minimal and divides up the  responsibilities across separate interfaces.


---

# 2.

Adapter is a design pattern applied in this design as it translates TaxReport's interface into the one Client actually needs (by converting the String into a PDF using PDFUtility), without modifying either class.


