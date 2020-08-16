#------------------------------------------#
# Title: CDInventory.py
# Desc: Starter Script for Assignment 05
# Change Log: Vakhtang Gurasashvili
# DBiesinger, 2020 august10 Created File
#------------------------------------------#
# TODO replace list of lists with list of dictsstrFileName = 'CDInventory.txt'  # data storage file

# Declare variabls
strChoice = '' # User input
Dict1 = {'ID#1': {'CD_Title' : 'Californication', 'Artist_Title': 'Red Hot Chili Peppers'}}  # list of data row
Dict2 = {'ID#2': {'CD_Title' : 'Common People', 'Artist_Title': 'Pulp'}}
lstTbl = [Dict1 , Dict2]  # list of dictionaries to hold data
Diction1={}
Cd_ID = ''
Line = 1
strChoice =''
strFileName = 'CDInventory.txt'
objFile = None  # file object
print('The Magic CD Inventory\n')
while True:
    # 1. Display menu allowing the user to choose:
    print('[l] load Inventory from file\n[a] Add CD\n[i] Display Current Inventory')
    print('[d] delete CD from Inventory\n[s] Save Inventory to file\n[x] exit')
    strChoice = input('l, a, i, d, s or x: ').lower()  # convert choice to lower case at time of input
    print()
# 5. Exit the program if the user chooses so
    if strChoice == 'x':
        break
    # TODO Add the functionality of loading existing data
    elif strChoice == 'l':
        lstRow = []
        objFile = open('CDInventory.txt','r')
        for line in objFile:
            lstRow = line.strip().split(',')
            print(lstRow)
        objFile.close()
        lstTbl.append(lstRow)
        pass
    # 2. Add data to the table (2d-list) each time the user wants to add data
    elif strChoice == 'a': 
        Usr_input0 = range(int(input('Please Enter How Many Entries You Have To Apply :\n')))
        for number in Usr_input0:
            Cd_ID = 'ID#{}'.format(number + 3)
            Usr_input1 = {'CD_Title': '{}'.format(input('cd title :'))}
            Usr_input2 = {'Artist_Title': '{}'.format(input('artist title :'))}
            Diction1[Cd_ID] = [Usr_input1, Usr_input2]
            number+=1
        lstTbl.append(Diction1)
        pass
        #for item in Diction1.items():
        #    lstTbl.append(item) Tried to separate 2 elements of user input dictionary :()
    elif strChoice == 'i':
        # 3. Display the current data to the user each time the user wants to display the data
        print('ID, CD Title, Artist')
        for row in lstTbl:
            print(row)
            print()
        print()
    elif strChoice == 'd':
        for row in lstTbl:
                print(Line,')',row)
                print()
                Line+=1
        print('To Delete Data Please Push apropriate line #:\n')
        Usr_del_choice = int(input())
        n = Usr_del_choice -1
        del lstTbl[n]
# 4. Save the data to a text file CDInventory.txt if the user chooses so
    elif strChoice == 's':
        strRow = ''
        objFile = open(strFileName, 'a')
        for row in lstTbl:
            strRow = str(row)
            objFile.write(strRow + '\n')
        objFile.close()
    else:
        print('Please choose either l, a, i, d, s or x!')
