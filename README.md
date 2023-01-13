- 👋 Hi, I’m @Jithin26
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Jithin26/Jithin26 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import difflib

# function to compare two documents
def compare_documents(doc1, doc2):
    # read the contents of each document
    with open(doc1, 'r') as file1, open(doc2, 'r') as file2:
        doc1_content = file1.read()
        doc2_content = file2.read()

    # compare the contents of the two documents
    difference = difflib.unified_diff(doc1_content.splitlines(), doc2_content.splitlines())
    return '\n'.join(difference)

# test the function
print(compare_documents('document1.txt', 'document2.txt'))
