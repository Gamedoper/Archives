---
layout: post
title:  "Visual Basic 6.0 Password Validation"
author: Jai
categories: [ Visualbasic6, Tutorial ]
image: assets/img/pwd.png
tags: [summer]
---




# Password Validation vb 6.0

        Private Function ValidatePassword(ByVal sPass) As Boolean
    Dim regEx
        
        Set regEx = CreateObject("vbscript.regexp")
        
        'At least 8 characters
        'At least 1 number
        'At least 1 lowercase letter
        'At least 1 uppercase letter
        'At least 1 special character. Special charaters include !@#$%^&+=
        regEx.Pattern = "^.*(?=.{8,})(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[!@#$%^&+=]).*$"
    
        ValidatePassword = regEx.Test(sPass)
        
        Set regEx = Nothing
    End Function
    
    Private Sub Command1_Click()
        MsgBox "Valid = " & ValidatePassword(Text1.Text)
    End Sub
    
    
    
    Private Sub Form_Load()
    Text1.Text = ""
    End Sub


**ONE TEXT BOX **
**ONE COMMAND BTN **

