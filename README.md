# hugo-mock-landing-page-autodeployed
The workflow added as gh-pages-deployment.yaml does the following:
1. Checks out the repository code and then fetches hugo themes (if there are any, in this case there is)
2. Using peaceiris it downloads the extended version of hugo setting up the hugo environment for our next step
3. utilizes the hugo command to setup the website with certain flags (-D includes draft content, --gc enables garbage collection, --minify minifies the output)
4. It then publishes our hugo server to GitHub pages utilizing the peaceiris/actions-gh-pages action. In this step is where we use our GitHub token (which is why we configured our repositories workflow settings the way we did)
