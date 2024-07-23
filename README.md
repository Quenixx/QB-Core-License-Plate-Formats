# QB-Core License Plate Formats
So basically, I’ve been searching for a long time about how to change the formats on license plates in qb, as I’ve been developing a Scandinavian server, I wanted the format “ABC 123” instead of GTAs random license plate formats, I’ve decided to share this with me which basically is a easy fix, but for those who don’t know and looking for it.

Basically you need to change the line in qb-vehicleshop/server.lua

the line to change is line 72 which is shown below

    local plate = QBCore.Shared.RandomInt(1) .. QBCore.Shared.RandomStr(2) .. QBCore.Shared.RandomInt(3) .. QBCore.Shared.RandomStr(2)

To understand this format (which is the deafault format ) is that it first created a random integer which is a number between 0-9, the second one is creating two random strings (RandomStr), and so on.

So lets say we wanted to change the license plate formats in our server to be swedish, which is "ABC 123"

we would have to change line 72 to this instead:

    local plate = QBCore.Shared.RandomStr(3) .. “ “ .. QBCore.Shared.RandomInt(3)

this will now give us 3 random Strings (RandomStr(3)) and three random numbers (RandomInt(3))

and the results should be something like 
JSU 716

To change to any format you like, just use this tutorial!

REMEMBER!

RandomStr gives random letters from A-Z

RandomInt gives random letters from 0-9
and you add brackets at the end and a number if you want several random letters or numbers, for example RandomStr(5) will give us a 5 random letters
