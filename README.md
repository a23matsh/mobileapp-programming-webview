
# Rapport
First I renamed my app by changing app_name in strings.xml. Then I enabled internet by going into AndroidManifest.xml
and adding the line of code <uses-permission android:name="android.permission.INTERNET" />. Then I replaced the existing TextView 
in activity_main_xml and created a webview element and named it "Main page". Then I enabled javascript execution 
"myWebView.getSettings().setJavaScriptEnabled(true);". Then I added a html page "about.html"

The following code snippet demonstrates how the user selections are made. The line int id = item.getItemId(); allows the application to retrieve the unique identifier i.e. which menu item was chosen.
Then there is 2 if statements one that checks for the external web page choice and one for the internal which are launched based on the choice made. If none of these are made the method calls the
default action.

@Override
public boolean onOptionsItemSelected(MenuItem item) {
    int id = item.getItemId();

    if (id == R.id.action_external_web) {
        showExternalWebPage();
        return true;
    }

    if (id == R.id.action_internal_web) {
        showInternalWebPage();
        return true;
    }

    return super.onOptionsItemSelected(item);
}

For example when the external page choice is made this line of code determines what is shown and in my case it's the HIS web page and the screenshot showing the execution
is attached as "External page.png".

public void showExternalWebPage(){
    myWebView.loadUrl("https://his.se");
}




Bilder läggs i samma mapp som markdown-filen.

![](Externalpage.png)
![](Internalpage.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
