V1 MyWork — GitHub frontend for Project Manager + Course Manager

DEPENDENCY
- Keep the existing V3 MyReader_API.gs installed.
- Keep Project.gs and Courses.gs unchanged.
- Same Apps Script deployment and same Authorized_Devices database are reused.

APPS SCRIPT
1. Add V1_MyWork_API.gs to the existing SecondBrain Apps Script project.
2. Open the existing MyReaderBridge.html and replace its contents with V5_MyReaderBridge.html.
3. Save. Deploy > Manage deployments > Edit > New version > Deploy.
4. No change to Article.gs/doGet is required; the existing ?bridge=myreader-v1 route is reused.

GITHUB
1. Create public repository: asjwd/mywork
2. Upload index.html, projects.html, courses.html, mywork-shim.js, portfolio-dark.css to repository root.
3. Settings > Pages > Deploy from branch > main > /(root).
4. Open https://asjwd.github.io/mywork/

AUTH
myreader and mywork share the same asjwd.github.io origin and the same device token keys. A browser already authorized in MyReader should normally open MyWork without another OTP.
