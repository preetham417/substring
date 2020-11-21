NO_OF_CHARS = 256

def max_distinct_char(str, n\p):

count = [0] * NO_OF_CHARS


for i in range(p):
    count[ord(str[i])] += 1

max_distinct = 0
for i in range(NO_OF_CHARS):
    if (count[i] != 0):
        max_distinct += 1

return max_distinct
def smallesteSubstr_maxDistictChar(str):

p = len(str)

# Find maximum distinct characters
# in any string
max_distinct = max_distinct_char(str, p)
minl = p


for i in range(p):
    for j in range(p):
        subs = str[i:j]
        subs_lenght = len(subs)
        sub_distinct_char = max_distinct_char(subs,
                                              subs_lenght)


        # 2. substing's length should be minimum
        if (subs_lenght < minl and
            max_distinct == sub_distinct_char):
            minl = subs_lenght

return minl
if name == "main":

str = input()

l = smallesteSubstr_maxDistictChar(str);
print( "The length of the smallest substring",
       "consisting of maximum distinct",
       "characters :", l)
