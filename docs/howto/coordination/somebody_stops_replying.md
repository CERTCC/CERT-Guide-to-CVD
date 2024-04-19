# Somebody Stops Replying

<!--start-->Sometimes one of the parties involved in a CVD effort will stop
responding. Often, this is simply a reflection of priorities and
attention shifting elsewhere rather than intentional behavior. It's
usually best to give the benefit of the doubt and keep trying to
reestablish contact if one of the CVD participants goes unresponsive.<!--end-->
Even in cases where the vendor has stopped responding in the midst of a
coordination effort, the CERT/CC recommends that reporters send the
vendor a "heads up" message with some lead time before publishing,
optionally including a draft of the document about to be published. This
helps the vendor prepare its communication plan if necessary, and
sometimes helps to identify any lingering misunderstandings on the
technical aspects of the vulnerability.

!!! example "Example: A 2015 Minecraft Vulnerability"

    Ammar Askar's [blog post](http://blog.ammaraskar.com/minecraft-vulnerability-advisory/){:target="_blank"}
    about a Minecraft vulnerability serves as an example where a quick heads up to
    the vendor could have avoided some confusion.

    > Update 2: The exact problem that caused this bug to go unpatched has been identified. 
    > Mojang attempted to implement a fix for this problem, however they did not test their fix against the proof of 
    > concept I provided, which still crashed the server perfectly fine. This, in combination with ignoring me when I 
    > asked for status updates twice led me to believe that Mojang had attempted no fix. In retrospect, a final warning 
    > before this full disclosure more recently was propbably in order. A combination of mis-communication and lack of
    > testing led to this situation today, hopefully it can be a good learning experience.

{% include-markdown "../recipes/_x06.md" heading-offset=1 %}
{% include-markdown "../recipes/_x10.md" heading-offset=1 %}

{% include-markdown "../../_includes/_report_certcc.md" heading-offset=1 %}
