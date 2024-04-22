!!! example "Mobile Supply Chain Example"

    !!! example inline end ""

        ```mermaid
        flowchart TD
            os[Mobile OS Vendor]
            phone[Mobile Phone Vendor]
            wireless[Wireless Carrier Vendor]
            customer[Customer]
            
            os --> phone
            phone --> wireless
            wireless --> customer
        ```

    Historically, the smartphone market provides a clear example of the effect of 
    the software supply chain on vulnerability response. 
    In a 2015 [blog post](https://insights.sei.cmu.edu/blog/supporting-android-ecosystem/){:target="_blank"},
    we discussed the complexity of the Android ecosystem and the challenges of coordinating vulnerability
    disclosure and patch deployment in that environment at the time.

    A vulnerability in a library component used in the Android
    operating system might have to be fixed by the library developer, then
    incorporated into the Android project by Google, followed by the device
    manufacturer updating its custom build of Android, and by the network
    carrier performing its customizations and testing before finally
    reaching the consumer's device. Each additional step between the party
    responsible for fixing the code and the system owner (the device user,
    in this case) reduces the probability that the fix will be deployed in a
    timely manner, if at all.

    A generalized example of the supply chain for some mobile devices
    is shown in the accompanying diagram.
