## URI Exploler: UpdateUserSchedule


### Based on [startustime API](https://stratustime.centralservers.com/service/home/library/)

Request 

```
<UpdateUserScheduleIn xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2.Contracts">
  <AuthToken>String content</AuthToken>
  <AutoAdd>true</AutoAdd>
  <Payload>
    <UpdateUserScheduleModel>
      <EmpIdentifier>String content</EmpIdentifier>
      <EnableHomeLaborLevelAssignment>true</EnableHomeLaborLevelAssignment>
      <EndDateTime>1999-05-31T11:20:00</EndDateTime>
      <PayTypeID>2147483647</PayTypeID>
      <StartDateTime>1999-05-31T11:20:00</StartDateTime>
      <LL01ID>2147483647</LL01ID>
      <LL02ID>2147483647</LL02ID>
      <LL03ID>2147483647</LL03ID>
      <LL04ID>2147483647</LL04ID>
      <LL05ID>2147483647</LL05ID>
      <LL06ID>2147483647</LL06ID>
      <LL07ID>2147483647</LL07ID>
      <LL08ID>2147483647</LL08ID>
      <LL09ID>2147483647</LL09ID>
      <LL10ID>2147483647</LL10ID>
      <LL11ID>2147483647</LL11ID>
      <LL12ID>2147483647</LL12ID>
      <LL13ID>2147483647</LL13ID>
      <LL14ID>2147483647</LL14ID>
      <LL15ID>2147483647</LL15ID>
      <ID>2147483647</ID>
    </UpdateUserScheduleModel>
    <UpdateUserScheduleModel>
      <EmpIdentifier>String content</EmpIdentifier>
      <EnableHomeLaborLevelAssignment>true</EnableHomeLaborLevelAssignment>
      <EndDateTime>1999-05-31T11:20:00</EndDateTime>
      <PayTypeID>2147483647</PayTypeID>
      <StartDateTime>1999-05-31T11:20:00</StartDateTime>
      <LL01ID>2147483647</LL01ID>
      <LL02ID>2147483647</LL02ID>
      <LL03ID>2147483647</LL03ID>
      <LL04ID>2147483647</LL04ID>
      <LL05ID>2147483647</LL05ID>
      <LL06ID>2147483647</LL06ID>
      <LL07ID>2147483647</LL07ID>
      <LL08ID>2147483647</LL08ID>
      <LL09ID>2147483647</LL09ID>
      <LL10ID>2147483647</LL10ID>
      <LL11ID>2147483647</LL11ID>
      <LL12ID>2147483647</LL12ID>
      <LL13ID>2147483647</LL13ID>
      <LL14ID>2147483647</LL14ID>
      <LL15ID>2147483647</LL15ID>
      <ID>2147483647</ID>
    </UpdateUserScheduleModel>
  </Payload>
</UpdateUserScheduleIn>

```

Response 

```
<UpdateUserScheduleOut xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2.Contracts">
  <Report>
    <APIVersion xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">String content</APIVersion>
    <ProcessTime xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">String content</ProcessTime>
    <RequestTime xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">1999-05-31T11:20:00</RequestTime>
    <ResponseTime xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">1999-05-31T11:20:00</ResponseTime>
    <Results xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">2147483647</Results>
  </Report>
  <Results>
    <UpdateResult xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">
      <ID>2147483647</ID>
      <Messages>
        <string xmlns="http://schemas.microsoft.com/2003/10/Serialization/Arrays">String content</string>
        <string xmlns="http://schemas.microsoft.com/2003/10/Serialization/Arrays">String content</string>
      </Messages>
      <Status>Failed</Status>
    </UpdateResult>
    <UpdateResult xmlns="http://schemas.datacontract.org/2004/07/AppOne.Services.V2">
      <ID>2147483647</ID>
      <Messages>
        <string xmlns="http://schemas.microsoft.com/2003/10/Serialization/Arrays">String content</string>
        <string xmlns="http://schemas.microsoft.com/2003/10/Serialization/Arrays">String content</string>
      </Messages>
      <Status>Failed</Status>
    </UpdateResult>
  </Results>
</UpdateUserScheduleOut>
```
