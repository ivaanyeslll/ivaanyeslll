- 👋 Hi, I’m @ivaanyeslll
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
ivaanyeslll/ivaanyeslll is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<macro name="2. Sample macro 3" icon="DOWNLOAD">

<assert-service description="Please, connect to a device with Generic Access service with Device Name characteristic. Service validation" uuid="00001800-0000-1000-8000-00805f9b34fb">

<assert-characteristic description="Ensure Device Name" uuid="00002a00-0000-1000-8000-00805f9b34fb">

<property name="READ" requirement="MANDATORY"/>

</assert-characteristic>

</assert-service>

<sleep description="This sample will demonstrate some very basic operations you can do using macros." timeout="400"/>

<read description="First, read the Device Name characteristic value." characteristic-uuid="00002a00-0000-1000-8000-00805f9b34fb" service-uuid="00001800-0000-1000-8000-00805f9b34fb"/>

<read description="Incoming data may also be validated." characteristic-uuid="00002a00-0000-1000-8000-00805f9b34fb" service-uuid="00001800-0000-1000-8000-00805f9b34fb">

<assert-value description="Let's check if Device Name equals 'Kaczka'." value-string="Kaczka"/>

</read>

<sleep description="Now the macro will wait 3 seconds..." timeout="3000"/>

<read-rssi description="...and read the RSSI of the connected device."/>

</macro>
