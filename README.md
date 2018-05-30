filename = 'pdf.pdf' # this var contents a filename
with open(filename, 'rb') as f: 
    s = f.read()  # reading file in a binary mode
counts = {}  # prepairing dictionary to store bytes and bytes' counts
for n in s:  
    counts[n] = counts.get(n, 0) + 1
li = counts.items()  # converting dictionary to list
li.sort(key=lambda x: 0-x[1])  # sorting list
