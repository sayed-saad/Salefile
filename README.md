# 1. File rename karo (agar capital hai)
git mv Index.html index.html

# 2. vercel.json banao
echo '{"rewrites":[{"source":"/(.*)","destination":"/index.html"}]}' > vercel.json

# 3. .gitattributes banao
echo '* text=auto
*.html text eol=lf
*.js text eol=lf
*.css text eol=lf' > .gitattributes

# 4. Push karo
git add .
git commit -m "fix: vercel 404 + add config files"
git push