# PGP/GPG Key Management

Separate from the issue of maintaining encryption keys for your
contacts, you must also maintain your own individual or organizational
encryption key.

PGP/GPG is a form of asymmetric encryption that makes use of two
different encryption keys called your *public key* and your *private
key*. The public key is intended to be shared; you advertise your public
key, and individuals or organizations wishing to contact you use your
public key to encrypt a message. Messages encrypted to your public key
can only be decrypted by the private key; therefore, it is important
that your private key stays private, and that no one outside of your
team or organization has access to this key.

A general discussion on encryption algorithms is beyond the scope of
this documentation, but at the time of this writing, it is recommended to
generate RSA keys with a length of at least 4096 bits to ensure security
into the near-to-moderate-term future.

## Use a Passphrase and Control Access

We recommend setting a strong passphrase on any key. Without a
passphrase, anyone who obtains the key file can immediately use the key
to sign messages or decrypt messages; if the private key is leaked to
unauthorized users but a passphrase was applied, then the user would
need to also know the passphrase before any damage could be done.

Of course, a persistent attacker could attempt to brute force the
phrase, so ideally the private key should be kept somewhere safe, out of
the hands of any unauthorized users. In other words, only members of the
CVD team should know the passphrase or even have access to the key file.
Ideally, if your CVD capability includes a dedicated communications
team, restrict knowledge of the passphrase and access to the key
material only to those members directly involved with communications. At
the CERT/CC, we have implemented this by having dedicated systems for
CVD communications work; private keys are only accessible from these
systems. In this setup, users must specifically request access and can
be allowed or denied based on need.

### Use Revocation Certificates and Key Rotation

A concern is that the private key may land into unauthorized hands. This
might occur in the event of a network breach, but another possibility is
a disgruntled former employee retaining a copy of the key. Because of
these possibilities, organizations using shared key material should
generate a revocation certificate for their PGP/GPG key and store it
somewhere safe. Obviously, it is important to restrict access to the
passphrase and revocation certificate; typically, it should only be
accessible by management. Should any emergency or security event occur,
you can publish the revocation certificate to notify the public to not
trust this key anymore. When a user imports your revocation certificate,
it marks the associated PGP/GPG key as unusable and untrustworthy.

To further mitigate these concerns, we recommended that you rotate
encryption keys (i.e., generate a new one) regularly. Some teams choose
to use the same key for two, three, or more years without change. This
recommendation arises to address concerns regarding the threat of
network breaches and the potential impact of losing control of the
private key. At the CERT/CC, we generate a new PGP/GPG key yearly.

Another reason to rotate keys is to revoke access to future encrypted
email when analysts leave the CVD team. The best way to do this is to
generate a new key whenever there are personnel changes; in this way,
future messages will be encrypted to the new key with a new passphrase,
and any former team members will be unable to access these messages even
if they still have access to the old key.

Regardless of how often you generate a new PGP key, your latest PGP
public key needs to be available to individuals and organizations so
that they may contact you. Be sure your key generation process includes
necessary steps to put your PGP public key in the public's hands. This
can consist of posting your PGP public key directly to your organization
website, or pushing your key to one of many PGP public key servers. You
can use these same mechanisms to distribute your revocation certificate
should the need arise.

## Practical Tips for Key Management

We wrap up this discussion with a review of recommended practices for
PGP/GPG key management:

- Generate an RSA key of at least 4096 bits.
- Restrict access to the private key material.
- Use a strong passphrase on the key.
- Restrict knowledge of the key passphrase to only those members of
    the CVD team involved in communications.
- Generate a revocation certificate for each key.
- Store the key passphrase and a revocation certificate in a safe
    location, such as a locked cabinet or safe in a secured area of the
    organization.
- Generate a new key whenever a member leaves the CVD team, and revoke
    the old key.
- Generate a new key periodically, regardless of other factors.
- Make your latest public key available in a known location to ensure
    recipients always have access to the latest key.
