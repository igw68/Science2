# Verificaiton motivations

Even a low-end car now has 100 electronic control units and over 100 million
lines of code. [https://spectrum.ieee.org/software-eating-car]

### Here is the article

IEEE.ORGIEEE XPLORE DIGITAL LIBRARYIEEE STANDARDSMORE SITES
SIGN INJOIN IEEE
FOR THE TECHNOLOGY INSIDER
Type to search

Explore by topic
IEEE websites place cookies on your device to give you the best user experience. By using our websites, you agree to the placement of these cookies. To learn more, read our Privacy Policy.

VIEW PRIVACY POLICY
ACCEPT & CLOSE
TRANSPORTATION
NEWS
How Software Is Eating the Car The trend toward self-driving and electric vehicles will add hundreds of millions of lines of code to cars. Can the auto industry cope? ROBERT N. CHARETTE07 JUN 202114 MIN READ
Photo of the inside of a car as seen from above.
ZF FRIEDRICHSHAFEN AG
    
AUTOMOTIVE SOFTWARE EMBEDDED SYSTEMS TEST AND MEASUREMENT VW EVS ECU AUTOMOBILES ADAS SELF-DRIVING CARS
Predictions of lost global vehicle production caused by the ongoing semiconductor shortage continue to rise. In January, analysts forecast that 1.5 million fewer vehicles would be produced as a result of the shortage; by April that number had steadily climbed to more than 2.7 million units, and by May, to more than 4.1 million units.

The semiconductor shortage has underscored not only the fragility of the automotive supply chain, but placed an intense spotlight on the auto industry’s reliance on the dozens of concealed computers embedded throughout vehicles today.

“No other industry is undergoing as rapid technological change as the auto industry,” says Zoran Filipi, Chair of the Department of Automotive Engineering at Clemson University’s International Center for Automotive Research. “This is driven by the need to address impending, evermore stringent CO2 and criteria emission regulations, while sustaining unprecedented rate of progress with development of automation and infotainment, and meeting the customer expectations regarding performance, comfort, and utility.” 

The coming years will see even greater change, as more auto manufacturers commit to phasing out their internal combustion engine (ICE) powered vehicles to meet global climate-change targets by replacing them with electric vehicles (EVs) that will eventually be capable of autonomous operation.

The past decade of ICE vehicle development illustrates the rapid progress it has made, as well as where it is heading.

Chart titled 'Vehicle production shortfall due to chip shortage.'CHART: MARK MONTGOMERY
“Once, software was a part of the car. Now, software determines the value of a car,” notes Manfred Broy, emeritus professor of informatics at Technical University, Munich and a leading expert on software in automobiles. “The success of a car depends on its software much more than the mechanical side.” Nearly all vehicle innovations by auto manufacturers, or original equipment manufacturers (OEMs) as they are called by industry insiders, are now tied to software, he says.

Ten years ago, only premium cars contained 100 microprocessor-based electronic control units (ECUs) networked throughout the body of a car, executing 100 million lines of code or more. Today, high-end cars like the BMW 7-series with advanced technology like advanced driver-assist systems (ADAS) may contain 150 ECUs or more, while pick-up trucks like Ford’s F-150 top 150 million lines of code. Even low-end vehicles are quickly approaching 100 ECUs and 100 million of lines of code as more features that were once considered luxury options, such as adaptive cruise control and automatic emergency braking, are becoming standard.

Additional safety features that have been mandated since 2010 like electronic stability control, backup cameras, and automatic emergency calling (eCall) in the EU, as well as more stringent emission standards that ICE vehicles can only meet using yet more innovative electronics and software, have further driven ECU and software proliferation.

Consulting firm Deloitte Touche Tohmatsu Limited estimates that as of 2017, some 40% of the cost of a new car can be attributed to semiconductor-based electronic systems, a cost doubling since 2007. It estimates this total will approach 50% by 2030. The company further predicts that each new car today has about $600 worth of semiconductors packed into it, consisting of up to 3,000 chips of all types.

Totaling the number of ECUs and lines of software only hints at the intricate electronic orchestration and software choreography found in vehicles today. By observing how they perform together, the extraordinary complexity that is meant to be invisible from a driver’s perspective begins to emerge. New safety, comfort, performance and entertainment features, the commercial imperative to offer scores of options to buyers resulting in a multiplicity of variants for each make and model, and the shift from gasoline and human drivers to electric and artificially intelligent drivers and the hundreds of millions of lines of new code that will need to be written, checked, debugged and secured against hackers, are making cars into supercomputers on wheels and forcing the auto industry to adapt. But can it? 

Features and Variants Drive Complexity
The drive over the last two decades to provide more safety and entertainment features has transformed automobiles from mere conveyances to mobile computing centers. Instead of racks of servers and high-speed optical interconnects, ECUs and wiring harnesses communicate data throughout the vehicle and beyond. And then there are the 10s of millions of lines code that run every time to you go to the grocery store.

Vard Antinyan, a software quality expert at Volvo Cars who has written extensively about software and system complexity, explains that as of 2020, “Volvo has a superset of about 120 ECUs from which it selects to create a system architecture present within every Volvo vehicle. Altogether, they comprise a total of 100 million lines of source code.” This source code, Antinyan says, “contains 10 million conditional statements as well as 3 million functions, which are invoked some 30 million places in the source code.” 

How much and what types of software resides in each ECU varies greatly, depending on, among other things, the computing capability of the ECU, the functions the ECU controls, the internal and external information and communications required to be processed and whether they are event or time triggered, along with mandated safety and other regulatory requirements. Over the past decade, more ECU software has been dedicated to ensuring operational quality, reliability, safety and security.

“The amount of software written to detect misbehavior to ensure quality and safety is increasing,” says Nico Hartmann, Vice President of ZF’s Software Solutions & Global Software Center at ZF Friedrichshafen AG, one of the world’s largest suppliers of automotive components. Where perhaps a third of an ECU’s software was dedicated to ensuring quality operations ten years ago, it is now often more than half or more, especially in safety critical systems, Hartmann states.

Which ECUs and associated software end up going into a Volvo like its luxury SUV XC90 model, which has approximately 110 ECUs, depends on several factors. Volvo, like all auto manufacturers, has variants of each model offered for sale aimed at different market segments. As Antinyan notes, “A person buying the exact same model Volvo in Sweden may not be identical to the one sold in the U.S.” Not only are there regional regulatory regimes that each car needs to meet, but each individual owner may choose among several optional engine, drive, safety, or other features that Volvo offers. Whatever configuration of standard, optional and legally required equipment is selected will determine the exact number and types of ECUs, software, and related electronics to be embedded into the vehicle, which all must be able to work together seamlessly. 

“Vehicle variant management is very difficult” for an auto manufacturer, says Antinyan, “because it involves everyone.” For instance, natural tension exists between the marketing department, which wants numerous types of vehicles possessing a myriad of features to offer to different customer segments, and the design and engineering departments, which would like fewer variants to help keep systems integration, testing, verification and validation efforts manageable. Each increase in functionality implies additional sensors, actuators, ECUs and accompanying software, and consequently extra integration efforts to ensure they work correctly.

Deloitte estimates that 40% or more of a vehicle’s development budget, from the start of its development to the beginning of production, can be attributed to systems integration, testing, verification and validation. Keeping track of all the current as well as legacy electronics and software in every model produced and sold can be a herculean task. Not surprisingly, efficiently managing variant complexity is a significant concern across the auto industry.

It will be no surprise, either, that connecting and powering all the ECUs, sensors and other electronic devices requires a great amount of wiring and manual effort to thread them through a vehicle. Thousands of wiring harness variants support vehicle customizations and multiple physical network busses to control the signal flow through a vehicle.

A vehicle’s physical electronic architecture poses more network design constraints to contend with. Many ECUs need to be close to the sensors and actuators they interact with, like the ECUs for braking systems or engine control. As a result, an automobile’s network harness, which can attach thousands of components, may contain more than 1,500 wires totaling 5,000 meters in length and weigh in excess of 68 kg. Reducing harness weight and complexity has become a major objective of automakers as ECUs, sensor and related electronic device numbers have grown. 

Testing Challenges
Even with the significant effort, time and monies being spent to ensure all the diverse electronic equipment works together, not every possible ECU build combination can be thoroughly tested before production starts. While a vehicle’s safety content tends to be mainly fixed, the ECU build complexity comes more in optional consumer comfort and convenience or performance functions. In some cases, because of a particular combination of optional features and functionality, “a vehicle rolling off the production line will be the first time that specific configuration was tested,” says Andy Whydell, ZF’s Vice President of Product Planning for Vehicle Systems.

Chart titled 'Electronic system as percent of total car cost.' CHART: MARK MONTGOMERY; SOURCE: DELOITTE TOUCHE TOHMATSU LIMITED
Some car makers have hundreds of thousands of potential build combinations of an individual vehicle model, if not more. To live test every combination of electronics possible in some car models, “would require a billion test set-ups,” he says. Multiple ECU build combinations, however, can be lab-tested using “bread-boards” by the OEMs during vehicle development, Whydell states, without needing to build a unique vehicle for each case.  

For even highly tested popular models, software-related errors are routinely found and corrected after they are sold. Sometimes the correction needs a correction, which happened to General Motors with the recall of its bestselling vehicle, the 2019 Chevy Silverado, along with its GMC Sierra light-duty trucks and Cadillac CT6. 

Making variant management more challenging, Whydell notes, is that “nearly all ECU design and software is outsourced to suppliers, with the OEM integrating the ECUs” to create a unified system from the desired customizable functionality. Whydell says that individual suppliers often do not have a great insight into how OEMs integrate ECUs together. Similarly, OEMs have limited insight into the software resident within the ECUs which are often acquired as a “black box” to support one of several functions such as infotainment, body and conform control, telematics, power train, or automated driver assist systems. 

How little software is developed by car makers is illustrated by comments made in 2020 by Herbert Diess, then CEO Volkswagen Group and now its Chairman, when he admitted that “hardly a line of software code comes from us.” VW estimates that only 10% of the software in its vehicles is developed in-house. The other 90%  is contributed by tens of suppliers, and at some OEMs, this number reportedly reaches more than 50. 

So many software suppliers, each with their own development approach, using their own operating systems and languages obviously adds another level of complication, especially in performing verification and validation. This is highlighted by a recent Strategy Analytics and Aurora Labs survey of software developers across the automotive supply chain asking how difficult it was to know when a code change in one ECU affects another. Some 37% of those surveyed indicated it was difficult, 31% indicated it was very difficult, 7% indicated that it was pretty darn close to impossible, while 16% indicated that it was not possible. 

Car companies and their suppliers are realizing that they must collaborate more to keep tighter control of data configuration management to keep unintended consequences from occurring due to unanticipated ECU code changes. But both admit that there is still a way to go. 

Stepping Up Security
Of course, automakers must ensure that the software is not only safe and reliable, but secure. Security researchers’ remote takeover of a 2014 Jeep Cherokee in 2015 was a wake-up call for the industry. Every supplier and OEM now recognizes the threat of lackluster cybersecurity; GM reportedly has 90 engineers working full-time on developing cybersecurity countermeasures.

However, a decade ago, “Vehicle software was designed for safety first. Security was a distant second,” says Mashrur Chowdhury, a vehicle cybersecurity expert and director of the U.S. Department of Transportation Center for Connected Multimodal Mobility at Clemson University. This is of note since much of the software designed ten or more years ago, when security was not the priority it is now, is still in use in ECUs today. 

“Potential attack surfaces are increasing virtually daily.”
Further, internal and external vehicle communications have exploded in the past decade. In 2008, there were an estimated 2,500 data signals being exchanged among the ECUs in a luxury car. Volvo’s Antinyan says that today more than 7,000 external signals connect the 120 ECUs in Volvo vehicles, and the number of internal vehicle signals being exchanged are two orders of magnitude greater. Consulting firm McKinsey & Company estimates this information can easily surpass 25 gigabytes of data an hour.

With the explosion of mobile apps and cloud-based services over the past ten years, not to mention the increasing complex electronics being built into vehicles themselves, “potential attack surfaces are increasing virtually daily,” says Chowdhury.  

Governments have taken note, too, and are placing several cybersecurity obligations on car makers. These include having a certified cybersecurity management system (CSMS), which requires each manufacturer to “demonstrate a risk-based management framework for discovering, analyzing and protecting against relevant threats, vulnerabilities, and cyber attacks.” 

Additionally, OEMs will need a software update management system to ensure over-the-air software updates are managed securely. Automakers are also being encouraged to “maintain a database of operational software component used in each automotive ECU, each assembled vehicle, and a history log of version updates applied over the vehicle’s lifetime.” This software bill of materials can help car makers quickly identify which ECUs and specific vehicles would be affected by a given cyber vulnerability.

The Soft Mechanic
Most drivers do not pay much attention to all the electronics arrays surrounding them—unless they are an annoyance or stop working. With electronic content increasing over the past decade, there have been plenty of opportunities for drivers to take notice of their vehicle’s electronics.

According to the 2020 Automotive Defect and Recall Report compiled by financial advisory firm Stout Risius Ross, 2019 was a record-setting year with 15 million vehicles recalled for electronic component defects. Half of the recalls involved software-based defects, the highest proportion Stout has measured since 2009.  

Chart titled 'Percentage of vehicles recalled due to electronic components defects.'CHART: MARK MONTGOMERY; SOURCE: STOUT RISIUS ROSS
Nearly 30% of the defects were related to software integration where a failure results from software interfacing with other electronic components or systems in a vehicle. Mitsubishi Motors recalled 60,000 SUVs because a software error in their hydraulic unit ECU interfered with multiple safety systems. 

Finally, more than 50% of the defects featured a failure that was not clearly caused by a software defect, but an update to the software was the remedy used. Ford Motor Company recalled certain models of its Fusion and Escape vehicles because coolant could enter their engine cylinder bores, which could permanently damage their engines. Ford’s fix was to reprogram the vehicles’ power-train control software to reduce the likelihood of coolant entering the engine cylinders. Stout’s data shows that occurrences of software being used to fix vehicle hardware problems has steadily increased in the past five years. 

“Recall sizes on average have been declining, and the average age of the vehicles have been declining, too,” says Neil Steinkamp, a Stout Managing Director. “Manufacturers are using technology to find defects sooner,” especially those involving electronics. Software-related defects tend to be found in newer vehicles, while ECU and other electronic component defects tend to emerge only after some time has passed since a vehicle’s introduction.

Stout Director Robert Levine notes that there has been a recent rise in component defects related to vehicle electronics “transitioning from owner convenience to safety critical components.” For instance, there has been a spate of back-up camera recalls in the U.S. since all vehicles manufactured after 1 May 2018 were mandated to provide drivers with a visible by 3 x 6 meter zone directly behind the vehicle. Many OEMs are finding that integrating more sophisticated camera software with other vehicle safety systems is proving difficult.

The operation of other new vehicle safety systems has not proceeded entirely smoothly, either. A study by the American Automobile Association (AAA) into advanced driving assistance systems that can help a driver with either steering or braking/accelerating demonstrated that these systems often disengage with little notice, instantly handing control back to the driver. Its tests showed that some type of issue appeared about every 13 km on average, including difficulty keeping a vehicle in its lane or coming too close to other vehicles or guardrails.

Climbing Costs of Repair 
Many car owners become aware of the increasing complexity of their vehicles when they have to pay for repairs. Nearly 60% of the labor costs to repair a collision involving a vehicle with advanced safety features results from the vehicle’s electronics. Even minor damage, say a cracked windshield that used to cost $210 to $220 has climbed to as much as $1,650 if the vehicle is equipped with a windshield-mounted camera for automatic emergency braking, adaptive cruise control, and lane departure warning systems, a 2018 AAA study shows. The expense of calibrating of all these systems, which is typically done manually, is a major cost driver.

Because even small miscalibrations of the sensors can drastically reduce the effectiveness of these safety features, “suppliers have developed auto alignment and auto calibration systems which can eliminate or simplify the manual process,” says ZF’s Whydell, helping drive up calibration accuracy while driving down repair costs.

Whydell also says suppliers and OEMS are looking at how to place sensors that tend to be mounted along a vehicle’s perimeter in places that are less likely to be damaged in an accident. AAA reports the cost to repair just a ultrasonic system located in the rear bumper that enables parking assistance to be around $1,300; if the rear radar sensors used for blind-spot monitoring and cross-traffic alerting were also damaged, another $2,050 in additional costs could be incurred for rear-end damage. 

With the cost of repair climbing due to electronics, it has reached the point where it is less costly for an insurance company to declare the vehicle a total loss. A recent report by claims management company Mitchell International says its data shows the average age of vehicles being declared a total loss has been dropping due to the repair cost of vehicle electronics. It expects the trend to continue as “vehicle complexity heightens,” the report states.

EV + AI = Unmanageable Complexity
Auto manufacturers are caught in a peculiar conundrum. According to the latest J.D. Power U.S. Vehicle Dependability Study, internal combustion engine vehicles today are the most dependable it has recorded in 32 years. They are also more comfortable, safer and less polluting. However, to address the increasing concerns of the government and the public over climate change across the globe, the manufacturers find themselves in the position of having to renounce their intricately crafted ICE vehicles in favor of electric vehicles that should be capable of autonomous driving capability sometime in the future.

Making their dilemma even more difficult is that, to develop EVs, manufacturers must leap across a software abyss.

In today’s vehicles, “software using today’s architectures is becoming unmanageable,” ZF’s Andy Whydell observes. Others echo that belief as well. According to consulting firm McKinsey & Company, software complexity in vehicles is rapidly outpacing the ability to both develop and maintain it. Software complexity grew by a factor of four over the past decade, but supplier and OEM software productivity has barely risen in the same time. Furthermore, software complexity is likely to rise by another factor of three over the next decade, it says. Car makers and suppliers alike are struggling to close the “development-productivity gap.” 

“Once, software was a part of the car. Now, software determines the value of a car.”
Part of the problem is supporting a steadily increasing code base, with one auto company leader telling McKinsey that at the current pace, software maintenance of the existing code base will consume all of its software R&D resources if the gap does not close. In fact, Whydell observes that, “In some cases, the auto industry doesn’t view total lines of code as a measure of complexity anymore, but the number of software personnel an OEM or supplier employs to meet current and future needs.” 

Closing the development-productivity gap looks particularly daunting, if, as Volkswagen Chairman Herbert Dies says, “Software will account for 90% of future innovations in the car.” Possessing the requisite software expertise will be a major key to success. As McKinsey has phrased it, “While automotive organizations must excel on many levels to win the software game, attracting and retaining top talent is probably the most crucial dimension.” It is little wonder why employing the right software expertise is “one of the things that keep me up at night,” admits ZF’s Whydell. It also is keeping every other supplier and OEM manager awake as well. 

OEMs have recognized belatedly, thanks in great part to Elon Musk’s software-defined car concept in the form of the Tesla, that their current approaches of outsourcing the requisite software and electronics to suppliers and then integrating them in ICE vehicles is not workable for EVs.

The functionality and complexity of the decentralized ECU architectures used in ICE vehicles “have reached their limits,” Tamara Snow, head of research and advanced engineering for Tier 1 auto supplier Continental AG is quoted in Wards Auto as saying. This is especially true if full autonomous driving capabilities require anywhere near the estimated 500 million or more lines of code.

“In some cases, the auto industry doesn’t view total lines of code as a measure of complexity anymore, but the number of software personnel an OEM or supplier employs to meet current and future needs.”
New vehicle software and physical architectures will be needed to manage banks of batteries instead of an internal combustion engine and associated drivetrain. The architecture will contain just a handful of powerful, extremely fast computer processors executing micro-services-driven code and communicate internally across a greater number of sensors across lighter wiring harnesses or even wirelessly, just for starters. External communication will be magnitudes greater as well. And these new architectures, ZF’s Hartmann points out, will need to be developed at low cost and at ever shortening time cycles by software teams in OEMs and suppliers that will be learning new methods for developing software and systems.

Probably the greatest problem is insufficient software expertise in the executive suites to understand the transformation needed, states Manfred Broy. While hardware complexity is the most visible aspect of a vehicle, Broy observes, “What I consider more significant is the complexity of software (which critically depends on the choice of the hardware) and in particular the cost of software, which is completely obscure to the OEMs and more critical because of its long term evolution.” Automotive executive suites are filled with “people of yesterday,” he says, “but they are still in charge.”

Clemson’s Zoran Filipi explains, “For over a hundred years, OEMs have focused on perfecting the internal combustion engine, outsourcing the rest of their vehicles to suppliers, and then integrating all the components together. The same approach was taken as electronics and software began to be used in vehicles—they were just another ‘black box’ to be integrated into a vehicle.”  Now, he says, “OEMs and their suppliers need to move their organizations from a hardware-first approach to a software-first mentality, all the while still supporting and improving ICE vehicles using their existing approaches for at least another decade.” 

Peter Mertens, former-head of Audi AG’s R&D and board member, stated in a recent interview with CleanTechnica, “The German auto industry gives their most critical new products, which will determine if they survive as companies in their existing structure, to the responsibility of managers who have the least experience and knowledge about their most critical part, the software.”

Mertens goes on to say that what is needed is a way to weed out executives that are not fit for their position. “Run a job assessment with all top managers at VW, Audi, Porsche, BMW, and Daimler tomorrow and ask them to code a small game or a simple but working virus,” he says. “If they are not able to do so, fire them immediately, because they are not fit for the job.” How many will be left, asks Mertens? The blood left on the floor will be a clue.

FROM YOUR SITE ARTICLES
As Electric Car Makers Ante Up Billions, Software Is Ace in the Hole ›
How and When the Chip Shortage Will End, in 4 Charts - IEEE Spectrum ›
Robert N. Charette
Contributing Editor Robert N. Charette is an acknowledged international authority on information technology and systems risk management. A self-described “risk ecologist,” he is interested in the intersections of business, political, technological, and societal risks. Along with being editor for IEEE Spectrum’s Risk Factor blog, Charette is an award-winning author of multiple books and numerous articles on the subjects of risk management, project and program management, innovation, and entrepreneurship. A Life Senior Member of the IEEE, Charette was a recipient of the IEEE Computer Society’s Golden Core Award in 2008.

PUBLISH
SORT BY
POPULAR
A black and white book-sized computer with a keyboard and monochrome LCD screen on top of a colorful background with bows
REVIEW
HANDS ON
COMPUTING
10 Gifts For Retrocomputing Fans
1 HOUR AGO8 MIN READ
 
An illustration showing an object shaped like a square peg in the field of view of a small box with a hole in the front. The box is mounted on a breadboard that also has a USB-connected microcontroller.
HANDS ON
SENSORS
Security With a Spectrometer
3 HOURS AGO5 MIN READ
 
An illustration of a face with an infinity symbol covering the face and people in VR goggles looking up and pointing. 
ANALYSIS
TELECOMMUNICATIONS
Meta Offers Nothing New to the Metaverse
17 DEC 20213 MIN READ
Related Stories
ARTIFICIAL INTELLIGENCE
INTERVIEW
SambaNova CEO: “We’re Built for Large”
 
COMPUTING
OPINION
Surviving the Robocalypse
 
OPINION
CONSUMER ELECTRONICS
The Chip Shortage Hurts Auto Sales a Lot, Consumer Electronics Only a Little
TRANSPORTATION
FEATURE
2021 TOP 10 TECH CARS
The trend toward all-electric is accelerating 
 LAWRENCE ULRICH26 MAR 20211 MIN READ    
Image of the Electric Hypercar from Rimac, the C Two.
PHOTO: RIMAC AUTOMOBILI
The COVID-19 pandemic put the auto industry on its own lockdown in 2020. But the technological upheavals haven't slowed a bit.

The march toward electric propulsion, for example, continued unabated. Nine of our 10 Top Tech Cars this year are electrically powered, either in EV or gas-electric hybrid form. A few critical model introductions were delayed by the virus, including the debut of one of our boldface honorees: the long-awaited 2021 Lucid Air electric sedan. It's expected to hit the market in a few months. But the constellation of 2021's electric stars covers many categories and budgets, from the ultra-affordable, yet tech-stuffed Hyundai Elantra Hybrid to the US $2.4 million Rimac C Two hypercar.

Keep Reading ↓

