# utl-optical-character-recognition-of-fuzzy-text-images-python-tesseract
Optical character recognition of fuzzy text images python tesseract .
    Optical character recognition of fuzzy text images python tesseract                                                                 
                                                                                                                                        
    If you have a clean image you can cevert(slide.bmp) to text using the command below                                                 
    x c:/progra~2/tesseract-ocr/tesseract d:/tesser/slide.bmp d:/tesser/slide.txt;                                                      
                                                                                                                                        
    Fuzzy input image                                                                                                                   
    https://tinyurl.com/ycer9j4c                                                                                                        
    https://github.com/rogerjdeangelis/utl-optical-character-recognition-of-fuzzy-text-images-python-tesseract/blob/master/picture.png  
                                                                                                                                        
    github                                                                                                                              
    https://tinyurl.com/ycyqzwjl                                                                                                        
    https://github.com/rogerjdeangelis/utl-optical-character-recognition-of-fuzzy-text-images-python-tesseract                          
                                                                                                                                        
    StackOverflow                                                                                                                       
    https://tinyurl.com/y946oo5p                                                                                                        
    https://stackoverflow.com/questions/54261255/pytesseract-cant-read-text-off-very-simple-image                                       
                                                                                                                                        
    also see                                                                                                                            
    https://github.com/rogerjdeangelis/utl_extract_text_from_images                                                                     
    https://tinyurl.com/ybxlf3mp                                                                                                        
                                                                                                                                        
                                                                                                                                        
    INPUT (fuzzy image of Gm)                                                                                                           
    =========================                                                                                                           
                                                                                                                                        
      __*_                                                                                                                              
     / ___|*   _ __ _*_                                                                                                                 
    * |* _   *| '_ ` _ \                                                                                                                
    | |_| |   | | | | | |                                                                                                               
     \____|   |_|*|_| |_|*                                                                                                              
       *                                                                                                                                
                                                                                                                                        
                                                                                                                                        
    EXAMPLE OUTPUT                                                                                                                      
    --------------                                                                                                                      
                                                                                                                                        
    %put &=frompy;                                                                                                                      
                                                                                                                                        
    FROMPY=Gm                                                                                                                           
                                                                                                                                        
                                                                                                                                        
    PROCESS                                                                                                                             
    =======                                                                                                                             
                                                                                                                                        
    %utl_submit_py64('                                                                                                                  
    import pytesseract;                                                                                                                 
    import cv2;                                                                                                                         
    import numpy as np;                                                                                                                 
    import pyperclip;                                                                                                                   
    pytesseract.pytesseract.tesseract_cmd = "C:/Program Files (x86)/Tesseract-OCR/tesseract";                                           
    from PIL import Image;                                                                                                              
    def url_to_image(url):;                                                                                                             
    .   resp = urllib.request.urlopen(url);                                                                                             
    .   image = np.asarray(bytearray(resp.read()), dtype="uint8");                                                                      
    .   image = cv2.imdecode(image, cv2.IMREAD_COLOR);                                                                                  
    .   return image;                                                                                                                   
    img = cv2.imread("d:/png/picture.png");                                                                                             
    retval, img = cv2.threshold(img,200,255, cv2.THRESH_BINARY);                                                                        
    img = cv2.resize(img,(0,0),fx=3,fy=3);                                                                                              
    img = cv2.GaussianBlur(img,(11,11),0);                                                                                              
    img = cv2.medianBlur(img,9);                                                                                                        
    cv2.imshow("asd",img);                                                                                                              
    cv2.waitKey(0);                                                                                                                     
    cv2.destroyAllWindows();                                                                                                            
    txt = pytesseract.image_to_string(img);                                                                                             
    print("recognition:", txt);                                                                                                         
    pyperclip.copy(txt);                                                                                                                
    ',return=frompy);                                                                                                                   
                                                                                                                                        
    %put &=frompy;                                                                                                                      
                                                                                                                                        
                                                                                                                                        
    OUPUT                                                                                                                               
    =====                                                                                                                               
    see above                                                                                                                           
                                                                                                                                        
                                                                                                                                        
    *_                                                                                                                                  
    | | ___   __ _                                                                                                                      
    | |/ _ \ / _` |                                                                                                                     
    | | (_) | (_| |                                                                                                                     
    |_|\___/ \__, |                                                                                                                     
             |___/                                                                                                                      
    ;                                                                                                                                   
                                                                                                                                        
    325   %utl_submit_py64('                                                                                                            
    326   import pytesseract;                                                                                                           
    327   import cv2;                                                                                                                   
    328   import numpy as np;                                                                                                           
    329   import pyperclip;                                                                                                             
    330   pytesseract.pytesseract.tesseract_cmd = "C:/Program Files (x86)/Tesseract-OCR/tesseract";                                     
    331   from PIL import Image;                                                                                                        
    332   def url_to_image(url):;                                                                                                       
    333   .   resp = urllib.request.urlopen(url);                                                                                       
    334   .   image = np.asarray(bytearray(resp.read()), dtype="uint8");                                                                
    335   .   image = cv2.imdecode(image, cv2.IMREAD_COLOR);                                                                            
    336   .   return image;                                                                                                             
    337   img = cv2.imread("d:/png/picture.png");                                                                                       
    338   retval, img = cv2.threshold(img,200,255, cv2.THRESH_BINARY);                                                                  
    339   img = cv2.resize(img,(0,0),fx=3,fy=3);                                                                                        
    340   img = cv2.GaussianBlur(img,(11,11),0);                                                                                        
    341   img = cv2.medianBlur(img,9);                                                                                                  
    342   cv2.imshow("asd",img);                                                                                                        
    343   cv2.waitKey(0);                                                                                                               
    344   cv2.destroyAllWindows();                                                                                                      
    345   txt = pytesseract.image_to_string(img);                                                                                       
    346   print("recognition:", txt);                                                                                                   
    347   pyperclip.copy(txt);                                                                                                          
    348   ',return=frompy);                                                                                                             
                                                                                                                                        
    NOTE: The file PY_PGM is:                                                                                                           
          Filename=i:\wrk\_TD6280_BEAST-PC_\py_pgm.py,                                                                                  
          RECFM=V,LRECL=32766,File Size (bytes)=0,                                                                                      
          Last Modified=25Jan2019:15:52:20,                                                                                             
          Create Time=25Jan2019:15:05:17                                                                                                
                                                                                                                                        
    import pytesseract                                                                                                                  
    import cv2                                                                                                                          
    import numpy as np                                                                                                                  
    import pyperclip                                                                                                                    
    pytesseract.pytesseract.tesseract_cmd = "C:/Program Files (x86)/Tesseract-OCR/tesseract"                                            
    from PIL import Image                                                                                                               
    def url_to_image(url):                                                                                                              
       resp = urllib.request.urlopen(url)                                                                                               
       image = np.asarray(bytearray(resp.read()), dtype="uint8")                                                                        
       image = cv2.imdecode(image, cv2.IMREAD_COLOR)                                                                                    
       return image                                                                                                                     
    img = cv2.imread("d:/png/picture.png")                                                                                              
    retval, img = cv2.threshold(img,200,255, cv2.THRESH_BINARY)                                                                         
    img = cv2.resize(img,(0,0),fx=3,fy=3)                                                                                               
    img = cv2.GaussianBlur(img,(11,11),0)                                                                                               
    img = cv2.medianBlur(img,9)                                                                                                         
    cv2.imshow("asd",img)                                                                                                               
    cv2.waitKey(0)                                                                                                                      
    cv2.destroyAllWindows()                                                                                                             
    txt = pytesseract.image_to_string(img)                                                                                              
    print("recognition:", txt)                                                                                                          
    pyperclip.copy(txt)                                                                                                                 
    NOTE: 22 records were written to the file PY_PGM.                                                                                   
          The minimum record length was 384.                                                                                            
          The maximum record length was 384.                                                                                            
    NOTE: DATA statement used (Total process time):                                                                                     
          real time           0.04 seconds                                                                                              
          cpu time            0.04 seconds                                                                                              
                                                                                                                                        
                                                                                                                                        
    i:\wrk\_TD6280_BEAST-PC_\py_pgm.py                                                                                                  
                                                                                                                                        
    NOTE: The infile RUT is:                                                                                                            
          Unnamed Pipe Access Device,                                                                                                   
          PROCESS=C:\Python27\python.exe i:\wrk\_TD6280_BEAST-PC_\py_pgm.py,                                                            
          RECFM=V,LRECL=32767                                                                                                           
                                                                                                                                        
    NOTE: 1 lines were written to file PRINT.                                                                                           
    NOTE: 1 record was read from the infile RUT.                                                                                        
          The minimum record length was 23.                                                                                             
          The maximum record length was 23.                                                                                             
    NOTE: DATA statement used (Total process time):                                                                                     
          real time           3.72 seconds                                                                                              
          cpu time            0.04 seconds                                                                                              
                                                                                                                                        
                                                                                                                                        
    NOTE: Fileref RUT has been deassigned.                                                                                              
    NOTE: Fileref PY_PGM has been deassigned.                                                                                           
                                                                                                                                        
    NOTE: Variable TXT is uninitialized.                                                                                                
    NOTE: The infile CLP is:                                                                                                            
          (no system-specific pathname available),                                                                                      
          (no system-specific file attributes available)                                                                                
                                                                                                                                        
    *******  Gm                                                                                                                         
    NOTE: 1 record was read from the infile CLP.                                                                                        
          The minimum record length was 2.                                                                                              
          The maximum record length was 2.                                                                                              
    NOTE: DATA statement used (Total process time):                                                                                     
          real time           0.00 seconds                                                                                              
          cpu time            0.00 seconds                                                                                              
                                                                                                                                        
                                                                                                                                        
    349   %put &=frompy;                                                                                                                
    FROMPY=Gm                                                                                                                           
                                                                                                                                        
