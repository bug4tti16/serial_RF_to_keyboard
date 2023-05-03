# serial_RF_to_keyboard
This code is to type in a member number corresponding to the RF card ID



TLDR. 
    set the port number -> make the CSV file -> Enjoy!!

Warning. 
    there is no encryption whatsoever, never use the program or the CSV file to store sensitive informantion.





I. before starting


  Make sure you know the port number your device is connected.
  
    Device manager -> Ports(COM-LPT) -> Device name(COM #)
    
    
        edit the reader.py file to the corresponding  COM #
        
        
            card_reader = 'COM#' (defult is set to COM5)
            
            
         
  
  Prepare CSV file.
    format: (order of items are negligable)
    
    
      Num, Name, RFID
      1, John, (set by card reader)
      .
      .
      .
      Num and name should be set manually, 
      you can use your existing user list file.
      cf) all the text is incoded to utf-8 (python default) change if needed

II. running the program 


  Run the windows batch file.
    reader.bat
    A command prompt window will stay open. (to close, close this window)
    *if you close this window the program will shut down*
    
  if a new card is read, the program will generate a input prompt(new card prompt).
  put in the member number to assign it to the member.
  
  the software will type the corresponding member number and press enter. 
  make sure the curser is where you want it to be.
  
III. Known bugs and errors.
  1. if you press cancel on the input prompt the code will crash. 
  code needs to be restarted.
  2. if multiple cards are read during the new card prompt. the software will freak out
  3. there is no delete feature buit in you can only overwrite.
  to delete, delete directly from the CSV file.
  
