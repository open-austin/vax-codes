# Vax.Codes - Free QR Codes for Covid-19 Vaccine Recipients

**WARNING: THIS PROJECT IS UNDER DEVELOPMENT AND DOES NOT WORK YET**

Website: https://vax.codes/

This website allows event organizers and businesses to instantly verify that someone has received a Covid-19 vaccine by scanning a QR code issued to the vaccine recipient by an approved health organization.

The goal of this project is to make it easy for organizations and businesses to re-open safely by incorporating vaccine verification into their admittance protocols.

## How it works

1. An "issuer" creates a QR code for a vaccinated person (can be emailed, printed, or texted)

2. The vaccinated person shows that QR code to the event organizer or business.

3. The event organizer or business scans the code, using any QR scanner app or https://vax.codes/scan

4. Scanning the QR code will open a URL with the person's name and verification they have received a Covid-19 vaccine.

5. The event organizer checks the name on the verification against the person's ID.

## Project status

See our [github issues](https://github.com/open-austin/vax-codes/issues) for the specific things we're working on.

### Phase 1 - Demo Ready
* [x] QR code scanner
* [x] QR code issuing (in browser)
* [x] Issuer admin
* [x] Issuer explorer/searching
* [ ] Group admin
* [x] Group explorer/searching
* [ ] Informational pages (how-it-works, about-us, etc.)
* [ ] Security overview page

### Phase 2 - Technical Features
* [ ] API docs
* [ ] Embedding scanner feature
* [ ] Embedding docs
* [ ] Local QR code issuing docs
* [ ] Self-hosting docs
* [ ] Other extra features (scanning uploaded pdfs, etc.)

### Phase 3 - Internationalization
* [ ] Multi-language support

## Limitations

The QR code *only* verifies someone with that name as having received a Covid-19 vaccine, so QR codes can be interchangeable between people with the same name.

The issuer may optionally include other information (such as birth date) when issuing the QR code, to increase uniqueness, but that is up to the issuer.

This limitation was deemed acceptable to ensure the protection of other confidential medical information.

## Privacy

Vax.Codes does *not* have a record of people who have received the Covid-19 vaccine.

Our website simply keeps a list of approved health organizations and verifies a QR code was issued by one of those organizations.

Names are stored directly in the QR codes themselves, and QR codes are generated by approved health organizations and given to vaccine recipients directly. So we never see them.

Also, the verification process happens entirely "client-side" (i.e. in your browser after you've loaded the URL), so our servers never see QR codes, even during verification.

Finally, this project is entirely open source, so security professionals can confirm that our website does exactly what is described and never gets any QR codes or personal information.

## Security

In the QR code, names are cryptographically signed by the approved health organization. So modifying the QR code to change the name will not work.

QR codes are "signed" by approved health organizations that can confirm that a person has received a Covid-19 vaccine. Each organization has one or more "signing keys" that they can use to issue new QR codes.

Vax.Codes works with government authorities and centralized health systems to maintain the list of approved health organizations and their signing keys.

(TODO: link to security document on how the signing/verification process works)

## Free and Open Source

This project was created by volunteers at [Open Austin](https://www.open-austin.org/), a brigade of [Code for America](https://www.codeforamerica.org/). The website code, list of approved health organizations, and project documentation are all free and open source.

This project follows Open Austin's [Code of Conduct](https://www.open-austin.org/about/#code-of-conduct).

Original project idea issue: [Project Idea #159](https://github.com/open-austin/project-ideas/issues/159)

