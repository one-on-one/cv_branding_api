# CV Branding

## API *(get)*

**Parameters:**

All query parameters typically passed to the call intake are expected for this API; most important are:

- leadid
- personal data (first\_name, last\_name, etc...)
- school or program specific data (program of interest, current education level, etc...)


**Example Requests:**
Base URI:
```
http://assure-quality.1on1.com/call_brand?
```

Base query params:
```
leadid=16884932748296924
&program=TSC
&program_2=
&vendorcode=OV.EDU_C.NICCV_S.GENX_R.INC_M.CI
&Email=SHRAMRAMPLE@GMAIL.COM
&email_1=SHRAMRAMPLE@GMAIL.COM
&Street=1509%20MORDOR%20ST
&address_1=1509%20MORDOR%20ST
&City=GRUMBLECAKES
&State=UT&Zip=23222
&Home_Phone=1234567891
&Phone2=
&Phone3=
&first_name=GUBSUMPLER
&last_name=SHRAMRAMPLE
&originator_id=168932648904328329920
&origin_tracking_code=
&audit_id=DAA-F49382j5FDFG-32C-4437478932784824678
&desireddegree=N
&hsgrad=2009
&birthyear=1990
&gender=M
&currentedlevel=HighSchool
&desiredstart=0
&military=N
&edu_currently_enrolled_elsewhere=N
&campusinterest=N
&repcode=618934274893729
```

Full Request (with all query params)
```
http://assure-quality.1on1.com/call_brand?leadid=162996924&program=TSC&program_2=&vendorcode=OV.EDU_C.NICCV_S.GENX_R.INC_M.CI&Email=SHRAMRAMPLE@GMAIL.COM&email_1=SHRAMRAMPLE@GMAIL.COM&Street=1509%20MORDOR%20ST&address_1=1509%20MORDOR%20ST&City=GRUMBLECAKES&State=UT&Zip=23222&Home_Phone=1234567891&Phone2=&Phone3=&first_name=GUBSUMPLER&last_name=SHRAMRAMPLE&originator_id=168932648329920&origin_tracking_code=&audit_id=DAA-0B5F-F5FDFG-324C-4437824678&desireddegree=N&hsgrad=2009&birthyear=1990&gender=M&currentedlevel=HighSchool&desiredstart=0&military=N&edu_currently_enrolled_elsewhere=N&campusinterest=N&repcode=3333333&
```

**Example Response:**


```json
{"call_brand":[
  [
    [
      32,
      "American InterContinental University CV 0.1"],
    [
      1044,
      "Colorado Technical University CV 0.1 HS/GED"]
    ],
    2
  ]
}
```

[Try Call Branding API](http://assure-quality.1on1.com/call_brand?no_prizm=true&no_leadid=true&leadid=162996924&status=Q&program=TSC&program_2=&vendorcode=OV.EDU_C.NICCV_S.GENX_R.INC_M.CI&Email=SHRAMRAMPLE@GMAIL.COM&email_1=SHRAMRAMPLE@GMAIL.COM&Street=1509%20MORDOR%20ST&address_1=1509%20MORDOR%20ST&City=GRUMBLECAKES&State=UT&Zip=23222&Home_Phone=1234567891&Phone2=&Phone3=&first_name=GUBSUMPLER&last_name=SHRAMRAMPLE&originator_id=168932648329920&origin_tracking_code=&audit_id=DAA-0B5F-F5FDFG-324C-4437824678&desireddegree=N&hsgrad=2009&birthyear=1990&gender=M&currentedlevel=HighSchool&desiredstart=0&military=N&edu_currently_enrolled_elsewhere=N&campusinterest=N&repcode=61729)

## Other Information
### MetaData fields
There are a number of data points collected to provide insight into how the API is performing, as well as providing robust feedback to users of the API and logging. Currenlty the only MetaData field provided for the user is `response_total`, which is measured in number of seconds for a full request. An example of the standared MetaData set that gets logged:

```json
{
  "metadata": [
    {
      "request_url": "VCID-PRIZM-PROSPECTOR:: http://assure-quality.1on1.com/call_brand?leadid=162996924&program=TSC&program_2=&vendorcode=OV.EDU_C.NICCV_S.GENX_R.INC_M.CI&Email=SHRAMRAMPLE@GMAIL.COM&email_1=SHRAMRAMPLE@GMAIL.COM&Street=1509%20MORDOR%20ST&address_1=1509%20MORDOR%20ST&City=GRUMBLECAKES&State=UT&Zip=23222&Home_Phone=1234567891&Phone2=&Phone3=&first_name=GUBSUMPLER&last_name=SHRAMRAMPLE&originator_id=168932648329920&origin_tracking_code=&audit_id=DAA-0B5F-F5FDFG-324C-4437824678&desireddegree=N&hsgrad=2009&birthyear=1990&gender=M&currentedlevel=HighSchool&desiredstart=0&military=N&edu_currently_enrolled_elsewhere=N&campusinterest=N&repcode=3333333&",
    "response_total": 11.085868,
    "response_qualify": "VCID-PRIZM-PROSPECTOR:: 7.798527"
    }
  ]
}
```

### Testing and other options
The API allows rpobust testing on our part and for that I have created a number of API options to allow us to test both performance and quality. If these options are used One On One cannot support the use of the results as valid.

