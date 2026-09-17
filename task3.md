The Design pattern this class implements is Factory. This is because the method inspects the input and correctly instantiates it to the right image type (Jpeg or Gif) and returns an object of that subtype. So the callers do not need to call "new" on a subclass directly.

# 1

The constructor is private because CreateImageReader only exists to be a Factory. It is never meant to be instantiated itself. By making it private, it prevents anyone from accidentally creating an instance of CreateImageReader that is useless

---

# 2.

The Java statement to read the Gif is:

ImageReader reader = CreateImageReader.createImageReader(fis);
