import Tablelt
import pandas as pd
import sys
import subprocess
import sys



from pandas import ExcelWriter
from pandas import ExcelFile
sys.stdout = open(r'C:\Users\nanjapa\Desktop\feb20\feb6\tGreyhoundRRP-result.txt',"w")

counter = 0
str2 = "------------------------------------------------------------------------"

strcom = "RRP-Comments/Response |" + '\n' + "                      |" +'\n' + "                      |" + '\n'

strfol = "Follow Up             |" + '\n' + "{GWIC Office Use Only}|" +'\n' + "                      |" + '\n'

result1 = pd.read_excel(r'C:\Users\nanjapa\Desktop\feb20\feb6\GreyhoundRRP-FullList.xlsx', sheet_name="Sheet1")
header_list = list (result1.columns.values)

for i, j in result1.iterrows():
    print (str2 + '\n')
    print(i , j)
    print(str2 + '\n'+ strcom + str2 + '\n' + strfol + str2 + '\n')
    #print()

header_list = list (result1.columns.values)



str1 =  str(counter +1) + "| " +  header_list[0]   +  "    | " + header_list[1] +  "          | " + header_list[2]  +  "      | " + header_list[3] +  "          | " +header_list[4] + "          | " + header_list[5] + "         | " +  header_list[6] +  "          | " +header_list[7] + "          | "
str2 = "-------------------------------------------------------------------------------------------------------------------------------------------------------------------"

#print ("|", header_list[0]  , "    |",header_list[1], "          |",header_list[2] , "      |",header_list[3], "          |",header_list[4], "          |",header_list[5],"         |", header_list[6], "          |",header_list[7], "          |")
str3 = "-------------------------------------------------------------------------------------------------------------------------------------------------------------------"
#print ( str2 + '\n' + str1 + '\n' + str3)

strcom = "RRP-Comments/Response |" + '\n' + "                       |" +'\n' + "                      |" + '\n'

strfol = "Follow Up             |" + '\n' + "{GWIC Office Use Only} |" +'\n' + "                      |" + '\n'

#print (strcom + str2 + '\n' + strfol + str2 + '\n')

sys.stdout.close()

#subprocess.call("grep -v Name: r'C:/Users/nanjapa/Desktop/feb20/feb6/tGreyhoundRRP-result.txt' > C:/Users/nanjapa/Desktop/feb20/feb6/tGreyhoundRRP-result1.txt", shell = True)


#Tablelt.printTable(header_list)






