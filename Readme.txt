Run the below command in conda in order to install the required packages
for /f %i in (requirements.txt) do conda install --yes %i 
FOR /F "delims=~" %f in (requirements.txt) DO conda install --yes "%f" || pip install "%f"

conda env export > assignment3env.yml

conda env create --name assignment3env -f=assignment3env.yml
