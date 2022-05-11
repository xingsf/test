import os,sys

def explore(dir):
    for root, dirs, files in os.walk(dir):
        print('debug: ', root, dirs, files) # 这行用来调试，帮助理解代码    
        for file in files:
            path = os.path.join(root, file)
            print(path)

 
def main():
    for path in sys.argv[1:]:           
        if os.path.isdir(path):
            explore(path)
			
			
if __name__="__main__":
    main()

            
