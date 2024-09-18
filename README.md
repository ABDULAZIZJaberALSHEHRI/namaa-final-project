# namaa-final-project
Abdulaziz Jaber Alshehri


- مشروع نماء:
(نماء) في اللغة العربية تعني الزيادة، وتتضمن الزيادة المستمرة كنمو الشجرة. هذا هو هدف المشروع، النمو. يهتم مشروع نماء بالاطفال في مرحلة نموهم من خلال توفير لهم التعلم والخبرة والتحديات. يحل هذا النظام مشكلة نقص المصادر لإيجاد برامج تستهدف المهارة المطلوبة للطفل. 
يجمع نظام نماء جميع مراكز الأنشطة من مختلف الأماكن و مختلف المهارات مثل: الرياضة والفن والأولمبياد والتعليم والمزيد. أيضا يمكن للوالديّن من خلال نظام نماء انشاء حسابات شخصية و إضافة أطفال تابعين لهم وتسجيلهم في برامج نشاطية و مسابقات ومتابعة أدائهم مع حصولهم  على شهادات عند اكمالهم البرنامج النشاطي.


- namaa project:
(Namaa) in Arabic means increase, and includes continuous increase like the growth of a tree. This is the goal of the project. Growth is concerned with young students until they grow up through learning, experience and challenges. This system solves the problem of the lack of resources for finding programs to target the child’s required skill. It brings together all activity centers from everywhere and all skills: sports, art, Olympics, education and more. It allows the parents to register their children, track their performance and receive certificates.



- namaa UseCase diagram:

![namaa useCase](https://github.com/user-attachments/assets/954193f9-cc6e-47b9-a3f5-bb120ce6f689)



-namma Class diagram:
[Namaa class diagram.pdf](https://github.com/user-attachments/files/17036485/Namaa.class.diagram.pdf)


- PostMan documnts Url:

- Figma Url: https://www.figma.com/design/NepUkGbwTIp0ClKUYY0evQ/Untitled?node-id=43-795&t=sr8VAQWjZwXIt156-1

- Presentation Url:

=====================================================================================

- My Endpoints and Models:

Models:
Center | Program | Advertisement | Certificate


Endpoints: 

CenterController:
- getAllCenters(@AuthenticationPrincipal User user);
- centerRegister(@Valid @RequestBody CenterDTO centerDTO);
- updateCenter(@AuthenticationPrincipal User user, @Valid @RequestBody CenterDTO centerDTO);
- updateCenter(@AuthenticationPrincipal User user, @Valid @RequestBody CenterDTO centerDTO);
- showMyCenterAccount(@AuthenticationPrincipal User user);
- changePassword( @AuthenticationPrincipal User user,@PathVariable String oldpassword, @PathVariable String 	newpassword);
- displayCenterFinancialReturn(@AuthenticationPrincipal User user);
- displayTotalNumberOfJoindChildren(@AuthenticationPrincipal User user);
- displayTotalNumberOfCenterProgram(@AuthenticationPrincipal User user);
- expandProgram(@AuthenticationPrincipal User user,@PathVariable Integer programid, @PathVariable LocalDate 	enddate);

ProgramController:
- addProgram(@AuthenticationPrincipal User user,@Valid @RequestBody Program program);
- getPrograms();
- updateProgram(@AuthenticationPrincipal User user,@PathVariable int programid,@Valid @RequestBody Program 	program);
- getMyProgramsByCenter(@AuthenticationPrincipal User user);
- displayChosedCenterPrograms(@PathVariable int centerid);
- setProgramStatus(@AuthenticationPrincipal User user,@PathVariable int programid,@PathVariable String status);
- deleteProgram(@AuthenticationPrincipal User user,@PathVariable int programid);
- deleteAllClosedPrograms(@AuthenticationPrincipal User user);
- displayProgramsFinancialReturns(@AuthenticationPrincipal User user,@PathVariable int programid);
- displayOpenPrograms();
- getProgrambyAge(@PathVariable int minage,@PathVariable int maxage);
- displayNumOfChildrenInTheProgram(@AuthenticationPrincipal User user,@PathVariable int programid);
- displayProgramsByDates(@PathVariable LocalDate startDate, @PathVariable LocalDate endDate);

CertificateController:
- getAllCertificates();
- getMyCertificate(@AuthenticationPrincipal User user,@PathVariable int childid);
- issueCertificate(@PathVariable Integer childId, @PathVariable Integer programId,@RequestBody Certificate 	certificateDetails);

AdvertisementController:
- addAdvert(@AuthenticationPrincipal User user, @RequestBody Advertisement advertisement);
- displayAllAdverts();
- approveAdvert(@AuthenticationPrincipal User user, @PathVariable Integer cid, @PathVariable Integer aid, 	@PathVariable LocalDate publishdate);
- getMyAdverts(@AuthenticationPrincipal User user);
- rejectAdvert(@AuthenticationPrincipal User user,@PathVariable Integer cid,@PathVariable int aid,@PathVariable 	String rejectreason);
- removeRejectedAdverts(@AuthenticationPrincipal User user);






