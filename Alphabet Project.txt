#working with dictionaries
alpha = 'abcdefghijklmnopqrstuvwxyz'
alpha = list(alpha)
aforapple = 'apple ball cat dog eliphant fox got horse ink jacle kitten lamb monkey nutritian orenge parot queen root station turtle udaan varun wonder xray yak zoo'
aforapple = aforapple.split(' ')
dictionary = dict(zip(alpha,aforapple))
print ("please enter alphabet here ")
while True:
    type = input('type single alphabet only or press enter to exit - ')
    if type.isdecimal():
        print ("""This is not alphabet, this is number.
Type alphabet or press enter again to exit""")
    elif type.lower() not in dictionary.keys():
            print("Sorry, it was not single alphabet.")
    else:
        if type == '':
            print ('press enter again to exit')
            type2 = input()
            if type2 == '':
                print("good bye")
                break
    
    
    if type.lower() in dictionary.keys():
        print ( type + " for " + dictionary[type.lower()])
    if type.lower() in alpha:
        if type == alpha[0]:
                    print ('"' + type + '"' + ' is first letter of the alphabet')
                    print ('"' + type + '"' + ' is followed by "' + alpha[1] +'"')
        elif type == alpha[-1]:
                print ('"' + type + '"' + ' is last letter of the alphabet')
                print ('"' + type + '"' + ' is preceeded by ' + alpha[-2])
        else:
            c = alpha.index(type.lower())+1
            d = alpha[alpha.index(type.lower())-1]
            e = alpha[c]
            if type.islower():
                print(type + ' or ' + type.upper() + ' is preceded by ' + d + ' or ' + d.upper())
                print(type + ' or ' + type.upper() + ' is followed by '+ e + ' or ' + e.upper())    
            else:
                print (type + ' or ' + type.lower() + ' is preceded by ' + d + ' or ' + d.upper())
                print(type + ' or ' + type.lower() + ' is followed by '+ e + ' or ' + e.upper()) 
