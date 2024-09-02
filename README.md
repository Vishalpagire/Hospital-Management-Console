using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;

namespace Project__Poona_Hospital
{
    public class Program//This class use  Declare the deparment
    {
        public Program()//This Constructor use the initiolization
        {
            Console.WriteLine("!!!..........-----------Poona Hospital & Research Centre----------..........!!! \n\n\t\t\t!!!___---...ISO 9001 : 2008___---...!!!\n\t\t\t!!!___---...NAHB Certified___---...!!!");
            Console.WriteLine("\n\t\t\tALL HANDS ON DECK!\n\t\t\tTHE DEDICATED TEAM IS\n\t\t\tWORKING AROUND THE CLOCK\n\t\t\tTO GET YOU THE BEST SERVICES");
            Console.WriteLine("\n\t\t\tCITY'S ONE OF THE BEST\n\t\t\tEMERGENCY AND TRAUMA UNIT");
            Console.WriteLine("\n\t\t\tTRADITION OF CARE\n\t\t\tPEPUTATION FOR EXCELLENCE\n\t\t\tSINCE : 1985\n");
            Console.WriteLine("\t\t\t.....'VISIT US'.....");
            Console.WriteLine("\n!!!.....--------------Welcome to Poona Hospital & Research Centre--------------- .....!!!");
        }

        public static void Main(string[] args)
        {
            
            Program program = new Program();

            while (true) // Loop to show menu continuously
            {
                Console.WriteLine("1. About Us : ");
                Console.WriteLine("2. Diagnostics : ");
                Console.WriteLine("3. Specialties : ");
                Console.WriteLine("4. Super Specialties : ");
                Console.WriteLine("5. Patient Guide : ");
                Console.WriteLine("6. Book Appointment :");
                Console.WriteLine("7. Contact Us : ");
                Console.WriteLine("8. Find Doctors : ");
                Console.WriteLine("9. Exit :");

                Console.WriteLine("Choose your corresponding Option : ");
                int option;
                if (int.TryParse(Console.ReadLine(), out option))

                    switch (option)//switch case use the check one condition and display
                    {
                        case 1:
                            AboutUs aboutUs = new AboutUs();
                            aboutUs.Display();
                            break;
                        case 2:
                            Diagnostics diagnostics = new Diagnostics();
                            diagnostics.Display();
                            break;
                        case 3:
                            Specialties specialties = new Specialties();
                            specialties.Display();
                            break;
                        case 4:
                            SuperSpecialties superSpecialties = new SuperSpecialties();
                            superSpecialties.Display();
                            break;
                        case 5:
                            PatientGuide patientGuide = new PatientGuide();
                            patientGuide.Display();
                            break;
                        case 6:
                            List<BookAppointment>appointments = new List<BookAppointment>();
                            while(true)
                            {
                                Console.WriteLine("1. Book Appointment");
                                Console.WriteLine("2. Display All Appointments");
                                Console.WriteLine("3. Exit");
                                Console.WriteLine("Enter Your Choice :"); ;
                                int choice= int.Parse(Console.ReadLine());

                                switch(choice)
                                {
                                    case 1:
                                        BookAppointment appointment = new BookAppointment();
                                        appointment.Patient_details();
                                        appointments.Add(appointment);
                                        Console.WriteLine("Your Appointment Is Succesfully......!!!");
                                        break;
                                }
                            }
                            
                        case 7:
                            ContactUs contactUs = new ContactUs();
                            contactUs.Display();
                            break;
                        case 8:
                            FindDoctors findDoctors = new FindDoctors();
                            findDoctors.Display();
                            break;
                        case 9:
                            Console.WriteLine("Back To Home...");
                            return; // Exit the loop and program


                        default:
                            Console.WriteLine("Invalid Option. Please, Try Again...");
                            break;
                    }
                else
                    Console.WriteLine("Invalide Choice. Please Enter The Number :");




            }
        }
    }




    public class AboutUs
    {
        public void Display()
        {
            
            Console.WriteLine("\nIntroduction: \nPoona Hospital & Research Centre is a multispecialty tertiary care hospital in Pune, providing the highest standard of clinical expertise and nursing care by offering the latest technology, and state-of-the-art hospital facilities. The Hospital focuses on rapid assessment, intervention, and treatment for numerous common and complex conditions.");
            Console.WriteLine("Poona Hospital & Research Centre presently has 300 beds and is situated in a central location, with easy access to the City.");
            Console.WriteLine("In addition to providing quality health care, the focus is also on preventive health programmes, medical education, and clinical research.");
            Console.WriteLine("Devotion to the art and science of healing reinforces every aspect of our mission.");
            Console.WriteLine("\nVision: \nTo be among the best hospitals for quality patient care and post-graduate medical education.");
            Console.WriteLine("\nMission: \nTo Provide Specialty and Super Specialty health care services to all sections of society at a reasonable cost.\n\n\n\n\n");
        }
    }





    public class Diagnostics
    {
        public void Display()
        {
            while (true)
            {
                Console.WriteLine("1. Audiology & Speech Therapy :");
                Console.WriteLine("2. Cardiology :");
                Console.WriteLine("3. Endoscopy :");
                Console.WriteLine("4. Pathology :");
                Console.WriteLine("5. Pulmonary Function Test (PFT) :");
                Console.WriteLine("6. Radiology :");
                Console.WriteLine("7. Ultrasonagraphy :");
                Console.WriteLine("8. CT-SCAN :");
                Console.WriteLine("9. Back To Home :");
                Console.WriteLine("Choose your corresponding Option: ");
                int option = Convert.ToInt32(Console.ReadLine());
                switch (option)
                {
                    case 1:
                        Console.WriteLine("Audiology & Speech Therapy :\nSounds consist of acoustic waves that are collected by the outer ear and amplified by the inner ear. Hearing is one of the most crucial of the five sensory organs since it allows us to communicate with the auditory world. Individuals with hearing problems should undergo complete hearing evaluations.Speech Therapy:The Department of Speech Therapy at Poona Hospital & Research Centre caters to any individual suffering from communication issues. This department has skilled professionals who would help you in overcoming challenges related to speech and basic skills.");
                        Console.WriteLine("The evaluation will also include recommendations from the audiologist regarding the choice of hearing aid for the patient.Oto Acoustic Emissions (OAE): Audiology Site Otoacoustic Emissions (OAE) is used as a screening tool for hearing in neonates or new born children. OAE test is very useful for the assessment of hearing defects in newborn babies and in children who are too young to cooperate in conventional hearing tests.Brainstem Evoked Response Audiometry (BERA): BERA is an objective test. In this test, evoked potentials in brain and the auditory pathway are collected from ongoing electrical activity with the help of electrodes placed over the scalp. BERA is used for newborn hearing screening, auditory threshold estimation, intraoperative monitoring, determining hearing loss type, degree, and auditory nerve and brainstem lesion detection.Immittance Audiometry (IA): IA is a measurement of the middle ear functions. It provides information about the movement of eardrum, status of middle ear and type of hearing loss.\n");
                        break;

                    case 2:
                        Console.WriteLine("Cardiology :\nThe Department of Cardiology at Poona Hospital & Research Centre is equipped with state-of-the-art equipment and a dedicated team of Cardiologists and Cath lab technicians with a wide experience in management of complex cardiac problems.Poona Hospital & Research Centre is a recognized institute by National Board of Examinations for DNB - Cardiology.\n");
                        Console.WriteLine("Diagnostics :\r\n* 4-D Color Doppler and Echocardiography including Transesophageal Echocardiography\r\n* Computerized stress analysis\r\nHolter monitoring\r\n* Ambulatory B.P. Monitoring\r\n* Coronary and Peripheral Angiography\r\n* Peripheral Colour Doppler\r\n* Transcranial Doppler\n");
                        break;

                    case 3:
                        Console.WriteLine("Endoscopy :\nThe Department of Endoscopy has a full complement of high-end equipment. An expert team of doctors and well-trained nurses ensure prompt services, and provide a wide range of diagnostic and therapeutic procedures as follows:\nAlso useful in mediastinal staging of documented lung malignancies, thus enabling the treating consultant to avoid surgical interventions in some patients.\n");
                        Console.WriteLine("1) .GI Endoscopy: Poona Hospital & Research Center offers various diagnostic procedures like:\r\n- Gastroscopy\r\n- Duodenoscopy\r\n- Colonoscopy\r\n- Oesophagoscopy\r\n- & several therapeutic procedures like:\r\n- Variceal Banding\r\n- Stricture Dilation\r\n- Sclerotherapy\r\n- Polypectomy\n");
                        break;

                    case 4:
                        Console.WriteLine("Pathology :\nThe Department of Pathology & Microbiology is an NABL accredited laboratory, which functions 24 X 7 with all fully automated equipments and test facilities available. With a dedicated, experienced and skilled team of Pathologists, Microbiologists and technicians available. The Lab is fully automated & bar-coded processes with periodically calibrated and interfaced equipments available. The Pathology Department also participates in various Internal & External quality assurance programmes- BIORAD USA, CMC VELLORE, ISHTM- AIIMS, BEQAS.The Pathology Laboratory is NABL accredited as per ISO 15189- 2012, since 2010, Certificate No- MC 2959This Department also caters to various primary care hospitals in this area for routine and specialized tests with complete assurance on precise diagnosis, monitoring and validation.\n");
                        Console.WriteLine("Services: \nThe majority of services included in the Pathology Department are as follows:\r\n- Specialized Hematology and Bone Marrow Examination\r\n- Clinical Biochemistry\r\n- Clinical Pathology\r\n- Immunoassays & Hormonal studies.\r\n- Autoimmune and infectious disease markers\r\n- Histopathology, cytology and Frozen sections.\r\n- Molecular Diagnostics includes Gene expert\n");
                        break;

                    case 5:
                        Console.WriteLine("Pulmonary Function Test (PFT) :\nPoona Hospital & Research Center has state-of-the-art chest labs with the most up-to-date technologies for assessing and diagnosing lung diseases, lung capacity, and cardiovascular pulmonary fitness. This test is usually useful for athletes. The lab is fully equipped with the latest high-end machines like:\n");
                        Console.WriteLine("Spirometry:\n Spirometry is helpful in assessing breathing patterns that identify conditions such as asthma, pulmonary fibrosis, cystic fibrosis, and COPD.\nImpulse Oscillometer: \nTo assess lung function in children and elderly patients who find it difficult to go through spirometry.\nCardiopulmonary test (CPX): \nTo assess the effect/impact of respiratory problem on cardiac state and vice versa used for testing lung and heart functioning before cardiac procedures.\r\nVyntus WALK: Offering a complete mobile solution to comfortably assess the functional exercise capacity of patients.\n");
                        break;

                    case 6:
                        Console.WriteLine("Radiology :\nThe Radiology Department at Poona Hospital & Research Center offers services 24X7. A well equipped department provides a wide range of diagnostic facilities like:\n");
                        Console.WriteLine("Digital Radiography:\n A state of the art machine which ensures least exposure and maximum patient comfort. Along with the image intensifer this machine enables various fluroscopic procedures.\n- Barium Studies\n- Retrograde Pyelography\n- Hysterosalpingography (HSG)\n- Endoscopic Retrograde Cholangiopancreatography (ERCP)\n- Computerised radiography System: Routine X-rays are taken quickly, the image is captured on software thereby facilitating prompt perusal and reporting.\n- Digital Mammography: This facilitates digital X- rays of the breast.\n- Computed Tomography Scan (CT scan): State-of-the-art VCT 64 CT Scan.\n-Magnetic Resonance Imaging: State of the art latest technology 3T MRI Scan\n-To support the diagnostic set up the Hospital also has multiple portable digital X-ray machines which can be used to take X-rays of patients in critical care units and other immobile patients admitted in the wards.\n");
                        break;

                    case 7:
                        Console.WriteLine("Ultrasonagraphy :\nThe USG Department uses an imaging techniques that employs high-frequency and sound waves to obtain images of structures within our body. With the latest and most advanced machinery available, remarkable results can be achieved at a higher resolution.\n");
                        Console.WriteLine("USG Guided Procedures:\n- Biopsy- Liver, Kidney, Breast Biopsy.\n- Fine Needle Aspiration Cytology (FNAC)- Thyroid, Breast, Lymph Node\n- MSK Sonography\n- Sono Mammography\n- Color Doppler\n- Portable Sonography.\n");
                        break;

                    case 8:
                        Console.WriteLine("CT-SCAN :CT scan department at Poona Hospital & Research Center is well equipped with an ultramodern CT scanner. The department provides accurate CT scan reports by our skilled and experienced team of radiologists. It offers services 24 X 7.\n");
                        Console.WriteLine("Services:\n- Brain (Plain)-CT scanning combines special x-ray equipment with sophisticated computers to produce multiple sliced images of organs.\n- Joints (Plain)- A computed tomography (CT) scan of the joints is an imaging method that uses x-rays to create detailed pictures of the Bone Joints.\n- Abdomen- A non-invasive painless radiological test to evaluate many disorders of the abdomen.\n- Angiography- The coronary angiography is a painless procedure that takes about 10 minutes it is usually done to check blood vessels. The process is similar to taking an x-ray.\n- Pulmonary- Clinical indications for CT pulmonary angiography have and continue to evolve based on research and new imaging.\n- CT Myelography- Myelography uses a real-time X-ray called fluoroscopy and an injection of contrast material to evaluate the spinal cord.\n");
                        break;

                    case 9:
                        return;

                    default:
                        Console.WriteLine("Invalid Option. Please, Try Again...");
                        break;
                }

            }
        }
    }





    public class Specialties
    {
        public void Display()
        {
            while (true) // Loop to show specialties menu continuously
            {
                Console.WriteLine("1. Ayurveda ");
                Console.WriteLine("2. Dialysis ");
                Console.WriteLine("3. Dermatology");
                Console.WriteLine("4. Ear Nose and Throat ");
                Console.WriteLine("5. Medicine ");
                Console.WriteLine("6. Orthopedics ");
                Console.WriteLine("7. Surgery ");
                Console.WriteLine("8. Back to Home");

                Console.WriteLine("Choose your corresponding Option: ");

                int option = Convert.ToInt32(Console.ReadLine());


                switch (option)
                {
                    case 1:
                        Console.WriteLine("Ayurveda department details...");

                        Ayurveda();
                        break;
                    case 2:
                        Console.WriteLine("Dialysis department details...");
                        Dialysis();
                        break;
                    case 3:
                        Console.WriteLine("Dermatology department details...");
                        Dermatology();
                        break;
                    case 4:
                        Console.WriteLine("Ear Nose and Throat department details...");
                        Ear_Nose_and_Throat();
                        break;
                    case 5:
                        Console.WriteLine("Medicine department details...");
                        Medicine();
                        break;
                    case 6:
                        Console.WriteLine("Orthopedics department details...");
                        Orthopadics();
                        break;
                    case 7:
                        Console.WriteLine("Surgery department details...");
                        Surgery();
                        break;
                    case 8:
                        return; // Exit the specialties loop
                    default:
                        Console.WriteLine("Invalid Option. Please, Try Again...");
                        break;
                }


            }
        }

        public void Ayurveda()
        {
            Console.WriteLine("Poona Hospital & Research Center has started Ayurvedic Department in 2019 with an objective of providing research and evidence based Ayurvedic treatment. The main aim here is to provide effective and economical healthcare services. The panel of experienced validays are Pioneers in Nadi Parikshan (Pulse reading) and best in their respective fields. We focus on each speciality and have on board Specialist Ayurvedic consultant for Respiratory disordess, Spine disordess, Skin disordess, Inferlitity, Diabetes etc. Department is well equipped with all the upgraded Panchakarma facilities and have in house medicine dispensing unit.The department organises various health related camps eg. Piles & Fistula with Ayurvedic Speciality of Ksharsutra, Agnikarma for pain management, Suvarna Prashan for children. With main focus on “Prevention, cure and wellness” we organise various public talks for awareness. To upgrade and enhance knowledge of Ayurvedic students and doctors department emphasise on conducting various CME.The ultimate moto is to provide the best possible service, heal the individual with classical ayurvedic treatment, maintain & retend the health of healthy one and to create awareness of Ayurveda at individual level.\n\n");
        }

        public void Dialysis()
        {
            Console.WriteLine("Haemodialysis & Renal Transplants:\nIn the busy haemodialysis unit, thousands of procedures are conducted every year. Trained staff also carries out haemodialysis in situ in the intensive care units. The hospital is a recognized centre for cadaver donor organ transplants\n\n");
        }

        public void Dermatology()
        {
            Console.WriteLine("The Department of Dermatology at Poona Hospital & Research Centre is dedicated to delivering superior, comprehensive skin care.\n");
            Console.WriteLine("Specialites :\n1.) Dr. H.S. Chopade\r\nDDV, M.D. (Skin)\r\nOPD Timing: Mon, Wed & Fri - 10.30am to 01.00pm\n\n2.) Dr. Rashmi Soni-Lohia\r\nM.D, DNB Derm.\r\nOPD Timing: Thurs - 10.30am to 01.00pm\n\n3.) Dr. Tanvi Komawar\r\nMBBS, DDV\r\nOPD Timing: Mon & Wed - 12.30pm to 2.30pm\n\n");
        }

        public void Ear_Nose_and_Throat()
        {
            Console.WriteLine("The department is equipped with machines to perform endoscopic examination and procedures.The team of highly trained doctors and experienced staff perform both basic & advanced surgical procedures for treating different problems ranging from punctured ear drum to acoustic neuroma.\n");
            Console.WriteLine("Specialites : \n1.)Dr. Arun Bahulikar\r\nM.D. (Medicine)\r\nOPD Timing: Wed - 10.30am to 01.00pm\n\n2.)Dr. V.G. Shah\r\nM.D. (Medicine), F.I.C. A (USA)\r\nOPD Timing: Thurs - 10.30am to 01.00pm\n\n3.)Dr. N.M. Beke\r\nM.D. (Medicine)\r\nOPD Timing: Mon - 10.30am to 01.00pm\n\n4.)Dr. S. V. Nagarkar\r\nM.D. (Medicine)\r\nOPD Timing: Thurs - 02.00pm to 04.30pm\n\n5.)Dr. Vandana Joshi\r\nM.S. (E.N.T)\r\nOPD Timing: Wed - 10.30am to 01.00pm\n\n6.)Dr. Shannu Tiwari\r\nMBBS, D.L.O\r\nOPD Timing: Tues - 02.00pm to 04.30pm\n\n7.)Dr. Amol Deshpande\r\nM.S (ENT)\r\nOPD Timing: Mon - 10.30am to 01.00pm\n\n8.)Dr. Poorva Lunawat\r\nMBBS, DORL, DNB(Otorhinolaryngolgy)\r\nOPD Timing: Thurs - 10.30am to 01.00pmn\n\n9.)Dr. Ajinkya Kelkar\r\nMBBS MS (Oto-Rhino-Laryn.)\r\nOPD Timing: Tues - 10.30am to 01.00pm\n\n9.)Dr. Ajinkya Kelkar\r\nMBBS MS (Oto-Rhino-Laryn.)\r\nOPD Timing: Tues - 10.30am to 01.00pm\n\n");
        }

        public void Medicine()
        {
            Console.WriteLine("The Medicine Department has a team of skilled physicians. The doctors provide highest quality of healthcare.Apart from utilizing their expertise in taking care of the ailing the team of expert senior doctors is also engaged in training the budding doctors. Poona Hospital & Research Centre is a recognized institute by National Board of Examinations for DNB- Medicine.\n");
            Console.WriteLine("Specialites : \n1.)Dr. Arun Bahulikar\r\nM.D. (Medicine)\r\nOPD Timing: Wed - 10.30am to 01.00pm\n\n2.)Dr. V.G. Shah\r\nM.D. (Medicine), F.I.C. A (USA)\r\nOPD Timing: Thurs - 10.30am to 01.00pm\n\n3.)Dr. N.M. Beke\r\nM.D. (Medicine)\r\nOPD Timing: Mon - 10.30am to 01.00pm\n\n4.)Dr. S. V. Nagarkar\r\nM.D. (Medicine)\r\nOPD Timing: Thurs - 02.00pm to 04.30pm\n\n");
        }
        public void Orthopadics()
        {
            Console.WriteLine("The department of Orthopaedics at Poona Hospital & Research Centre provides the advanced treatment and surgical procedures. The team comprises of highly experienced orthopaedic surgeons backed by well trained staff. The surgeons have expertise in diagnosing and treating the problem of the joints, muscles, ligaments, bones, nerves, and tendons.Some of the Salient Features of this department are:The department has a dedicated Shoulder Arthroscopy Clinic. Arthroscopy is a minimally invasive surgery. In comparison to the traditional approach it offers fewer complications, faster recovery period, and less scarring.The department also has a specialized OPD for treatment of several joint problems, osteo arthiritis, frozen shoulder, ligament injuries (ACL & PCL) The surgeons have expertise in handling complex trauma & joint problems Specialites\n");
            Console.WriteLine("Specialites : \n1.)Dr. Rajan D. Kothari\r\nM.Ch (Ortho)\r\nOPD Timing: Mon & Thurs - 10.30am to 01.00pm\n\n2.)Dr. Ashok N. Desai\r\nM.Ch (Ortho)\r\nOPD Timing: Tues - 10.30am to 01.00pm\n\n3.)Dr. Jayant Shah\r\nMS (Ortho)\r\nOPD Timing: Fri - 10.30am to 01.00pm\n\n4.)Dr. Siddharth Shah\r\nMBBS, D Ortho, DNB\r\nOPD Timing: Wed - 10.30am to 01.00pm\n\n5.)Dr. Sujit Kadrekar\r\nDNB ortho, D. ortho, MNAMS\r\nFellowship in Arthroscopy & Shoulder Surgery (Korea)\r\nOPD Timing: Sat - 10.30am to 01.00pm\n\n");
        }

        public void Surgery()
        {
            Console.WriteLine("The Department of Surgery at Poona Hospital & Research Center deals with a range of surgical ailments and emergencies. In addition to managing common surgical problems, the surgeons are adept at complex abdominal surgeries. Most abdominal surgeries are performed through laparoscopy (keyhole surgery) Supporting this team of highly skilled surgeons are trained nurses and state-of-the-art operation theatres.\n");
            Console.WriteLine("Specialites : \n1.)Dr. R.S. Dumbre\r\nM.S. (Gen. Surg)\r\nOPD Timing: Mon - 10.30am to 01.00pm\n\n2.)Dr. Prafulla Pradhan\r\nM.S. (Gen. Surg)\r\nOPD Timing: Mon - 02.00pm to 04.30pm\n\n3.)\r\nDr. Arun Fernandes\r\nM.S. (Gen. Surg)\r\nOPD Timing: Tues, Thurs & Sun - 10.30am to 01.00pm\n\n4.)Dr. Bharat Dikshit\r\nM.S. (Gen. Surg)\r\nOPD Timing: Fri - 10.30am to 01.00pm\n\n");
        }

    }
}





public class SuperSpecialties
{
    public void Display()
    {
        while (true) // Loop to show specialties menu continuously
        {
            Console.WriteLine("1. Nephrology ");
            Console.WriteLine("2. Urology ");
            Console.WriteLine("3. Oncology ");
            Console.WriteLine("4. Endocrinology ");
            Console.WriteLine("5. Head and Neck Oncology ");
            Console.WriteLine("6. Back to Home");



            Console.WriteLine("Choose your corresponding Option: ");
            int option = Convert.ToInt32(Console.ReadLine());


            switch (option)
            {
                case 1:
                    Console.WriteLine("Nephrology department details...");
                    Nephrology();
                    break;
                case 2:
                    Console.WriteLine("Urology department details...");
                    Urology();
                    break;
                case 3:
                    Console.WriteLine("Oncology department details...");
                    Oncology();
                    break;
                case 4:
                    Console.WriteLine("Endocrinology department details...");
                    Endocrinology();
                    break;
                case 5:
                    Console.WriteLine("Head_and_Neck_Oncology department details...");
                    Head_and_Neck_Oncology();
                    break;
                case 6:
                    return;

                default:
                    Console.WriteLine("Invalid Option. Please, Try Again...");
                    break;
            }


        }
    }

    public void Nephrology()
    {
        Console.WriteLine("The Department of Nephrology at Poona Hospital & Research Centre offers comprehensive treatment for all types of kidney disorders. The team of senior Nephrologists and experienced technicians ensures safe treatment of all Nephrological issues with a focus on improving the quality of life.The hospital is a recognised centre for cadaver donor organ transplants.Paediatric Nephrology:- The Pediatric nephrology unit at Poona Hospital & Research Centre offers diagnosis and treatment to children suffering from urinary and kidney disorders.\n");
        Console.WriteLine("Specialites : \n1.) Dr. S.V. Ukidve\r\nM.D. (Medicine)\r\nOPD Timing: Tues : 11:30am to 01:30pm\n\n2.) Dr. N.C. Ambekar\r\nDNB (Nephrology)\r\nOPD Timing: Mon & Fri - 11.30am to 01.30pm\n\n3.) Dr. Sunil Jawale\r\nDM Nephrology\r\nOPD Timing: Wed & Sat - 11.30am to 01.30pm\n\n4.) Dr. Nikhil Rathi\r\nNephrology)\r\nOPD Timing: Sat 2.00pm to 04.30pm\n\n");
    }
    public void Urology()
    {
        Console.WriteLine("The Department of Urology offers comprehensive diagnostic and treatment services for urological conditions like kidney stones, urinary tract strictures, cancers, etc. The state-of-the-art urology unit offers minimally invasive, scarless options for urologic procedures and medical management of kidney disease.The Urology Laser unit at Poona Hospital & Research Centre ensures Lithotripsy with higher success rate and decreased chance of steinstrasse (complication where a column of stone fragments blocks the ureter), less intraoperative bleeding, shorter catherization time, shorter hospital stays and lower transfusion rates.\n");
        Console.WriteLine("Specialites : \n1.) Dr. Shirish Bhave\r\nDNB Urology\r\nOPD Timing: Mon & Thurs - 11.30am to 01.30pm\n\n2.) Dr. Jaydeep Date\r\nM.Ch Urology\r\nOPD Timing: Wed & Fri - 11.30am to 01.30pm\n\n 3.) Dr. Sandesh Surana\r\nDNB Urology\r\nOPD Timing: Tues & Sat - 11.30am to 01.30pm\n\n");
    }
    public void Oncology()
    {
        Console.WriteLine("The department of Oncology at Poona Hospital & Research Centre comprises of both medical & surgical oncology. This department offers treatment of cancers through surgery & chemotherapy.The chemotherapy is monitored by trained doctors & assisted by well qualified nurses.\n");
        Console.WriteLine("Specialites : \n1.) Dr. Amit Bhatt\r\nMD (Med),DNB (Med) Fellowship (Oncology), Medical Oncologist\r\nOPD Timing: Mon - Sat - 11.30am to 01.30pm\n\n2.) Dr. Saurabh Mohite\r\n(Onco Surgery)DNB (Gen. Surg)\r\nOPD Timing: Wed,Thurs & Sat - 11.30am to 01.30pm\n\n");
    }
    public void Endocrinology()
    {
        Console.WriteLine("The Department of Endocrinology at Poona Hospital offers comprehensive services in diagnosis, treatment and management of all hormone related disorders.\n");
        Console.WriteLine("Specialites : \n Dr. Mohan Magdum\r\nD.M. (Endocrinology)\r\nOPD Timing: Mon & Fri - 11.30am to 01.30pm\n\n");
    }

    public void Head_and_Neck_Oncology()
    {
        Console.WriteLine("The Head & Neck Oncology Department offers highly qualified and trained professionals consisting of head & neck surgeons, Plastic surgeons, medical oncologist, Cytopathologist, Dentist, speech & swallow therapist and Physiotherapist .\n");
        Console.WriteLine("- They are adept in providing expert and comprehensive care to patient with cancers of:\n- Oral cavity - Lip, tongue, gums, Floor of the mouth , Buccal mucosa\n- Tonsils\n- Pharynx (Throat)\n- Larynx (Voice box)\n- Salivary glands\n- Lymph nodes in the neck\n- Nasal cavity & sinuses\n- Ear\n- Thyroid & Parathyroid glands\n");
        Console.WriteLine("Specialites : \n Dr. Shivprakash Mehta\r\nMBBS,MS(Otorhinolaryngology), Fellow in Hand & Neck Surgical Oncology\r\nOPD Timing: Mon & Thurs - 02.00pm to 04.30pm\n\n");
    }


}





public class PatientGuide
{
    public void Display()
    {
        while (true) // Loop to show specialties menu continuously
        {
            Console.WriteLine("1. Insurance ");
            Console.WriteLine("2. Registration/Admission ");
            Console.WriteLine("3. Billing ");
            Console.WriteLine("4. Room Category ");
            Console.WriteLine("5. Attendant and Visitors ");
            Console.WriteLine("6. Back to Home");



            Console.WriteLine("Choose your corresponding Option: ");
            int option = Convert.ToInt32(Console.ReadLine());


            switch (option)
            {
                case 1:
                    Console.WriteLine("Insurance department details...");

                    Insurance();

                    break;
                case 2:
                    Console.WriteLine("Registration/Admission details...");
                    Registration_Admission();

                    break;
                case 3:
                    Console.WriteLine("Billing department details...");

                    Billing();

                    break;
                case 4:
                    Console.WriteLine("Room Category details...");
                    Room_Category();


                    break;
                case 5:
                    Console.WriteLine("Attendant and Visitors details...");
                    Attendant_and_Visitors();

                    break;

                case 6:
                    return;

                default:
                    Console.WriteLine("Invalid Option. Please, Try Again...");
                    break;
            }



        }
    }

    public void Insurance()
    {
        Console.WriteLine("Insurance Companies : \n - Apollo Munich Health Insurance Co. Ltd.\n- ICICI Prudential Life Insurance Co ltd.\n- Reliance General Insurance Co.Ltd.\n- Bajaj Allianz General Insurance\n- Iffco Tokia General Insurance Co.Ltd.\n- Religare General Insurance Co.Ltd.\n- Cholamandalam MS General Insurance\n- Future Generali (I) Insurance Co. Ltd.\n- Star Health & Allied Insurance Co.Ltd\n- ICICI Lombard General Insurance Co.\n- Max Bupa Health Insurance Co. Ltd.\n\n");
        Console.WriteLine("- The hospital has tie ups with the following corporate companies\n- harat Forge Ltd\n- Citi bank\n- Cummins India Ltd\n- Hindustan Unilever Ltd\n- Kirloskar Oil Engines Ltd\n- Lawson Toubro\n- Reserve Bank of India\n- State Bank of India\n- Tata Motors Ltd\n- Tata Technologies Pvt Ltd\n- Max Bupa Health Insurance Co. Ltd\n- Atlas Copco Ltd\n- Bank of India\n- BSA corp. Ltd\n- Cummins Diesels Sales Services\n- JCB India Ltd\n- KSB Pumps ltd\n- Kimberly-clerks lever ltd.\n- Sudarshan Chemical Ind. Ltd\n- Thermax Ltd.\n- Thermax Workmen Medical Trust\n- Thyssenkrupp Industries Ltd.\n- Union Bank of India\n- Pravin Masalewale (Suhana)\n");
        Console.WriteLine("DO’S : \n - Obtain pre - authorization form the TPA counter, located on the first floor of the hospital, 3 - 4 days prior to the admission for planned hospitalization.\n- Please carry the following documents when you come to obtain the preauthorization for cashless facility.\n- 1. I card issued by the TPA / Insurance company\n- 2. One photo I.D.\n- 3. Current year policy papers.\n- 4. Previous investigations / Prescriptions / Other details regarding any treatment may be required depending upon the ailment for which cashless is being sought.\n- Pre - authorization form is to be filled in by treating doctor.\n- Check about the pre - authorization approval at the TPA counter within next 24hrs.\n- You can avail cashless treatment at the hospital after receipt of written authorization from TPA for the covered ailment.\n- Leave back all the original documents and signed claim form with the hospital at the time of discharge.\n- Contact TPA counter in case of any query.\n- The policy holder has to bear the expenses which are not covered under the terms and conditions of the policy.\n");
        Console.WriteLine("DON’TS : \n- Don’t insist upon admission at the hospital merely for investigation, evaluation or Health check - up as these are not approved by TPAs.\n- Don’t insist on cashless facility for planned admissions at the Hospital without obtaining the pre- authorization approval from TPA.\n- Don’t carry back any original documents at the time of discharge from the hospital, if your cashless is approved by the TPA.\n- Don’t forget to sign your bill of hospitalization and your discharge card.\n- The investigators from the TPA / Insurance company often visit the hospital to check on the patient anytime till the final sanction is received.\n- Don’t insist on leaving the hospital prior to receipt of final sanction from the insurance company / TPA.\n");

    }

    public void Registration_Admission()
    {
        Console.WriteLine("In an Emergency Just dial 020-66096000\n- Our ambulance will reach you as soon as possible. Our emergency and trauma unit is manned 24 x 7 by trained staff and doctors.\n- If you are coming into our Emergency and Trauma Unit, if possible please bring with you: a list of your current medications any x-rays/ultrasounds/scans that may be related to your condition Latest / Last prescription of your treating doctor Your Identity proof / insurance card / Govt I card / Company I card Please be aware that patients are seen in order of severity of their illness, and not in order of attendance If another patient comes to the Emergency & Trauma Unit with a more serious condition, you will be required to wait. We thank you for your patience and understanding.\n");
        Console.WriteLine("Registration / Admission : \n - Courteous staff at the reception and admissions counter will greet and guide you through the entire process.\n- Once at the admission desk you will be required to fill a form specifying details of the patient. A unique Patient PH Number will be issued to you on submission of then duly filled registration form. This number will be required to be produced by you, every time you visit the hospital for easy and effective traceability of your previous medical records.\n- Please note that people who are insured / govt employees or have their companies pay for their medical expense are requested to clarify all details with your respective insurance agent / company before Admission. For any further assistance on the same you can get in touch with our TPA Helpdesk / PRO office . If the patient wishes to avail any facility like cashless admission under insurance cover etc… the same must be specified in the form.\n- You also need to specify the name of the consultant you wish to admit your patient under. The admission desk will also let you know the room rent as applicabl\n\n");
        Console.WriteLine("Your Room : /n- The hospital currently has 300 beds. Standard in-patient accommodation ranges from General ward to Luxury rooms. We are happy to discuss your individual choice of accommodation prior to admission\n");
        Console.WriteLine();
    }

    public void Billing()
    {
        Console.WriteLine("Billing Estimate:-/n - Ask for approximate estimate of expenses which will be incurred for the treatment/ the admission.\n- The treatment plan must be endorsed by the treating doctor. However please note the estimate is just an approximate figure and may increase/decrease as per your actual treatment.\n- The expenditure structure provided is for a planned treatment protocol as desired by the doctor in the patients best interest. It is likely to increase if your treatment protocol changes and any unplanned emergency surgical procedures or unexpected ICU stay is required for providing the best healthcare to the patient. Your attendants must discuss your condition with the treating doctor on daily basis and keep updated on the course of treatment being followed.\n");
        Console.WriteLine("Deposit:-/n- You are requested to deposit certain advance at the time of admission. The amount will vary as per the accommodation.\n- As and when the bill exceeds the deposited amount, You will be requested to make appropriate deposits. You can ask for an interim bill if you need so for any clarification\n- One of our Public Relation Assistants will approach you and request to make appropriate deposits time to time. Your cooperation with our staff will be highly appreciated.\n- All financial transactions are accepted in the form of cash, credit/debit card and demand draft only. Payment in the form of cheques is not acceptable\n");
        Console.WriteLine("Billing Cycle:-\n- Billing Cycle is from 12 midnight to 12 midnight the next day\n- For more details and clarification, PRO may be contacted to help you\n");
    }

    public void Room_Category()
    {
        Console.WriteLine("Room Retaining : \n- If there are no other patients waiting for admission , permission for the room retaining may be granted. However the discretion lies entirely on the hospital whether or not to allow room retaining.\n- On the event of retaining the allotted room, charges as per tariff plan will be levied in addition to the bed occupied by the patient.\n- In case room is not retained by attendants then patient will be allotted same or another room of suitable category on return from OT/Post-Operative Ward or ICU, subject to availability.\n- Refund If there is any balance remaining with the hospital at the time of discharge then refund shall be made after your discharge.\n- Refund up to Rs.9,999 will be made immediately in cash.\n- Any refund above Rs. 10000 shall be made in cheque.\n- Original payment receipt needs to be shown at the cash counter for availing refund.\n\n");
        Console.WriteLine("ISSUE : \n Room Allotment / transfer / up gradation :- Front office executive\n");
        Console.WriteLine("ISSUE : \n Billing Related Queries :- PRO\n\n");
    }

    public void Attendant_and_Visitors()
    {
        Console.WriteLine("Attendant_and_Visitors :\n* On admission each patient will be issued one attendant pass. Kindly ensure you collect it from the admission desk Attendants must always carry their pass while leaving the In-Patient premises. They may not be allowed inside if they are unable to produce the attendant pass at the entrance on their return.\n* Attendants/visitors are requested not to argue with the security staff if they are not allowed to enter the In-Patient premises. They are doing their duty to make your patients stay comfortable and safe.\n* Visitors other than the attendant shall be allowed only during visiting hours. Visitors are strictly restricted in critical care units.\n");
        Console.WriteLine("MORNING : \n12.00 noon to 1.00 p.m.\n\n EVENING : 4.30p.m. to 7.00p.m.\n\n");
    }

}





public class BookAppointment
    {
        public int Age;

        public string Name, Surname, Adress, Message, Consern, DoctorName;

        public void Patient_details()
        {
            Console.WriteLine("Enter The First Name :");
            Name = Console.ReadLine();
            Console.WriteLine("Enter The Last Name :");
            Surname = Console.ReadLine();
            Console.WriteLine("Enter The Address :");
            Adress = Console.ReadLine();
            Console.WriteLine("Enter The Age :");
            Age = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter Your Specific Consern :");
            Consern = Console.ReadLine();
            Console.WriteLine("Enter Your Doctors Name :");
            DoctorName = Console.ReadLine();
            Console.WriteLine("Enter Your Message :");
            Message = Console.ReadLine();
        }
        public void Display_details()
        {
            Console.WriteLine("Name : " + Name);
            Console.WriteLine("Surname : " + Surname);
            Console.WriteLine("Adress : " + Adress);
            Console.WriteLine("Age : " + Age);
            Console.WriteLine("Consern : " + Consern);
            Console.WriteLine("Your Message : " + Message);
            Console.WriteLine("Your Doctor is : " + DoctorName);
            Console.WriteLine("!!!..........Your Appointment Book Successfully..........!!!\n \n ");


        }
    }





public class ContactUs
{
    public void Display()
    {
        Console.WriteLine("Contact information here...\n");
        Console.WriteLine("Address Info: \nPoona Hospital & Research Center, 27 Sadashiv Peth, Nr. Alka Talkies, Pune 411030, Maharashtra\n");
        Console.WriteLine("Call us on: \nFor Emergency : 020 66096000\nFor Appointment : +91 97305 59600\n\n");
    }
}





public class FindDoctors
{
    public void Display()
    {
        Console.WriteLine("Finding Doctors...\n");

        Console.WriteLine("Select Specialites...\n\n");

        while (true) // Loop to show specialties menu continuously
        {
            Console.WriteLine("1. All Speciality ");
            Console.WriteLine("2. Chardiology ");
            Console.WriteLine("3. Chest Desease ");
            Console.WriteLine("4. Dental ");
            Console.WriteLine("5. Dermatology ");
            Console.WriteLine("6. Ear Nose And Throat ");
            Console.WriteLine("7. Endicronology ");
            Console.WriteLine("8. Head and Neck ");
            Console.WriteLine("9. Nephrology ");
            Console.WriteLine("10.Nurology ");
            Console.WriteLine("11.NeuroSergery ");
            Console.WriteLine("12. Oncology");
            Console.WriteLine("13. Orhtopadices ");
            Console.WriteLine("14. Radiology ");
            Console.WriteLine("15. Urology ");
            Console.WriteLine("16. Back to Home");



            Console.WriteLine("Choose your corresponding Option: ");
            int option = Convert.ToInt32(Console.ReadLine());


            switch (option)
            {
                case 1:
                    Console.WriteLine("All Speciality Doctors details...\n");

                    All_Speciality();

                    break;
                case 2:
                    Console.WriteLine("Chardiology Doctors details...\n");
                    Cardiology();

                    break;
                case 3:
                    Console.WriteLine("Chest Desease Doctors details...\n");
                    Chest_Desease();


                    break;
                case 4:
                    Console.WriteLine("Dental Doctors details...\n");

                    Dental();

                    break;
                case 5:
                    Console.WriteLine("Dermatology Doctors details...\n");
                    Dermatology();

                    break;

                case 6:
                    Console.WriteLine("Ear Nose and Throat Doctors details...\n");
                    Ear_Nose_Throat();

                    break;

                case 7:
                    Console.WriteLine("Endicronology Doctors details...\n");
                    Endicronology();

                    break;
                case 8:
                    Console.WriteLine("Head_and_Neck Doctors details...\n");
                    Head_and_Neck();

                    break;
                case 9:
                    Console.WriteLine("Nephrology Doctors details...\n");
                    Nephrology();

                    break;
                case 10:
                    Console.WriteLine("Nurology Doctors details...\n");
                    Nurology();

                    break;
                case 11:
                    Console.WriteLine("NeuroSergery Doctors details...\n");
                    NeuroSergery();

                    break;
                case 12:
                    Console.WriteLine("Oncology Doctors details...\n");
                    Oncology();

                    break;
                case 13:
                    Console.WriteLine("Orhtopadices Doctors details...\n");
                    Orhtopadices();

                    break;
                case 14:
                    Console.WriteLine("Endicronology Doctors details...\n");
                    Radiology();

                    break;
                case 15:
                    Console.WriteLine("Endicronology Doctors details...\n");
                    Urology();

                    break;

                case 16:
                    return;

                default:
                    Console.WriteLine("Invalid Option. Please, Try Again...\n");
                    break;
            }
        }
    }
    public void All_Speciality()
    {
        Console.WriteLine("Dr. (Ms.) Aarti Shahade\nM.D. (Medicine)\nOPD Timing: Tues – 02.00pm to 04.30pm\n\nDr. (Ms.) Neela Desai\nM.S. (Obst & Gynae)\nOPD Timing: Thurs & Sat – 10.30am to 01.00pm\n\nDr. Ms Vaibhavi Rawal\nDr. (Ms.) Vaibhavi Rawal\nM.S. (Ophthal)\nOPD Timing: Mon & Fri – 10.30am to 01.00pm\n\nDr. Abbas Chopdawala\nDNB (Med)\nOPD Timing: Fri – 10.30am to 01.00pm, Sat – 02.00pm to 04.30pm\n\nDr. Abhijit Joshi\nDiploma in Orthopaedics, Fellowship in Diabetic Foot\nOPD Timing: Mon & Wed – 02.00pm to 4.30pm\n\n");
    }

    public void Cardiology()
    {
        Console.WriteLine("Dr. Prasad Shah\nDr. Prasad Shah\nDNB (Card), DM (Card)\nOPD Timing: Fri – 11.00am to 1.30pm\n\nDr. Madhusudhan Asawa\nDNB Cardiology\nOPD Timing: Mon & Thurs – 11.00am to 1.30pm\n\nDr. Chandrakant Chavan\nDr. Chandrakant Chavan\nDNB Cardiology\nOPD Timing: Sat – 11.00am to 1.30pm\n\nDr. Hasmukh Gujar\nDr. Hasmukh Gujar\nDNB Cardiology\nOPD Timing: Tues – 11.00am to 1.30pm\n\nDr. Vivek Gaikwad\nDr. Vivek Gaikwad\nDNB Cardiology\nOPD Timing: Sat – 02.00pm to 04.30pm\n\nDr. Ashish Trivedi\nDNB Cardiology\nOPD Timing: Tues & Thurs – 02.00pm to 04.30pm, Sun – 11.00am to 1.30pm\n\n");
    }
    public void Chest_Desease()
    {
        Console.WriteLine("Dr. Nitin Abhyankar\nMD, ERS Diploma\nOPD Timing: Mon, Web & Fri – 11.30am to 01.30pm\n\nDr. Jayashree Jain\nMBBS DTCD\nOPD Timing: Sun – 11.30am to 01.30pm\n\nDr. Vrushali Khirid\nDNB (Gen Med), DTCD\nOPD Timing: Tues & Sat – 11.30am to 01.30pm\n\n");
    }
    public void Dental()
    {
        Console.WriteLine("Dr. Mukund Kothawade\nB.D.S., M.D.S. (Prosthodontics)\nOPD Timing: Mon,Wed,Fri & (2nd Sat) – 12.30pm to 02.30pm\n\nDr. Paresh Gandhi\nB.D.S., M.D.S (Prosthodontics) OPD Timing: Mon – 9.30am to 11.30am, Tues and Thurs – 12.30pm to 2.30pm\n\nDr. Akshita Solanki\nB.D.S., M.D.S (Periodontics)\nOPD Timing: Fri – 9.30am to 11.30am\n\nDr. Amruta Naik\nB.D.S., M.D.S.(Paediatrics Dentist)\nOPD Timing: Thurs – 03.30pm to 05.30pm\n\nDr. Anjali Gandhi\nB.D.S, M.D.S (Conservative Dentisty\nOPD Timing: Tue – 9.30am to 11.30am, Sat – 3.30pm to 5.30pm\n\nDr. Pushkar Gadre\nB.D.S., M.D.S (Oral and Maxillofacial Surgery)\nOPD Timing: Wed – 03.30pm to 05.30pm");
    }
    public void Dermatology()
    {
        Console.WriteLine("Dr. H.S. Chopade\nDDV, M.D. (Skin)\nOPD Timing: Mon, Wed & Fri – 10.30am to 01.00pm\n\nDr. Rashmi Soni-Lohia\nM.D, DNB Derm.\nOPD Timing: Thurs – 10.30am to 01.00pm\n\nDr. Tanvi Komawar\nMBBS, DDV\nOPD Timing: Mon & Wed – 12.30pm to 2.30pm\n\n");
    }

    public void Ear_Nose_Throat()
    {
        Console.WriteLine("Dr. Vandana Joshi\nM.S. (E.N.T)\nOPD Timing: Wed – 10.30am to 01.00pm\n\nDr. Shannu Tiwari\nMBBS, D.L.O\nOPD Timing: Tues – 02.00pm to 04.30pm\n\nDr. Amol Deshpande\nM.S (ENT)\nOPD Timing: Mon – 10.30am to 01.00pm\n\nDr. Poorva Lunawat\nMBBS, DORL, DNB(Otorhinolaryngolgy)\nOPD Timing: Thurs – 10.30am to 01.00pm\n\n");
    }

    public void Endicronology()
    {
        Console.WriteLine("Dr. Mohan Magdum\nD.M. (Endocrinology)\nOPD Timing: Mon & Fri – 11.30am to 01.30pm\n\n");
    }

    public void Head_and_Neck()
    {

        Console.WriteLine("Dr. Shivprakash Mehta\nMBBS,MS(Otorhinolaryngology), Fellow in Hand & Neck Surgical Oncology,\nOPD Timing: Mon & Thurs – 02.00pm to 04.30pm\n\n");
    }

    public void Nephrology()
    {
        Console.WriteLine("Dr. S.V. Ukidve\nM.D. (Medicine)\nOPD Timing: Tues : 11:30am to 01:30pm\n\nDr. N.C. Ambekar\nDNB (Nephrology)\nOPD Timing: Mon & Fri – 11.30am to 01.30pm\n\nDr. Sunil Jawale\nDM Nephrology\nOPD Timing: Wed & Sat – 11.30am to 01.30pm\n\n");
    }
    public void Nurology()
    {
        Console.WriteLine("Dr. S.V. Ukidve\nM.D. (Medicine)\nOPD Timing: Tues : 11:30am to 01:30pm\n\n");
    }
    public void NeuroSergery()
    {
        Console.WriteLine("Dr.-Sushil-Patkar.\nDr. Sushil Patkar\nM.Ch (Neurosurg)\nOPD Timing: Tues,Thurs & Sat : 11.30am to 01.30pm\n\nDr.-Nikhil-Talathi.jpg\nDr.Nikhil Talathi\nM.Ch (Neurosurg)\r\nOPD Timing: Wed : 11.30am to 01.30pm\n\n");
    }

    public void Oncology()
    {
        Console.WriteLine("Dr.-Pradeep-Bafna\nDr. Pradeep Bafna\nM.Ch (Neurosurg)\nOPD Timing: Mon & Fri : 11.30am to 01.30pm\n\nDr. Sushil Patkar\nM.Ch (Neurosurg)\nOPD Timing: Tues,Thurs & Sat : 11.30am to 01.30pm\n\nDr.-Nikhil-Talathi.jpg\nDr.Nikhil Talathi\nM.Ch (Neurosurg)\nOPD Timing: Wed : 11.30am to 01.30pm\n\n");
    }

    public void Orhtopadices()
    {
        Console.WriteLine("Dr. Shivprakash Mehta\nMBBS,MS(Otorhinolaryngology), Fellow in Hand & Neck Surgical Oncology,\nOPD Timing: Mon & Thurs – 02.00pm to 04.30pm\n\n");

    }
    public void Radiology()
    {
        Console.WriteLine("Dr. (Ms.) Aarti Shahade\nM.D. (Medicine)\nOPD Timing: Tues – 02.00pm to 04.30pm\n\nDr. (Ms.) Neela Desai\nM.S. (Obst & Gynae)\nOPD Timing: Thurs & Sat – 10.30am to 01.00pm\n\nDr. Ms Vaibhavi Rawal\nDr. (Ms.) Vaibhavi Rawal\nM.S. (Ophthal)\nOPD Timing: Mon & Fri – 10.30am to 01.00pm\n\nDr. Abbas Chopdawala\nDNB (Med)\nOPD Timing: Fri – 10.30am to 01.00pm, Sat – 02.00pm to 04.30pm\n\nDr. Abhijit Joshi\nDiploma in Orthopaedics, Fellowship in Diabetic Foot\nOPD Timing: Mon & Wed – 02.00pm to 4.30pm\n\n");
    }
    public void Urology()
    {
        Console.WriteLine("Dr. (Ms.) Aarti Shahade\nM.D. (Medicine)\nOPD Timing: Tues – 02.00pm to 04.30pm\n\nDr. (Ms.) Neela Desai\nM.S. (Obst & Gynae)\nOPD Timing: Thurs & Sat – 10.30am to 01.00pm\n\nDr. Ms Vaibhavi Rawal\nDr. (Ms.) Vaibhavi Rawal\nM.S. (Ophthal)\nOPD Timing: Mon & Fri – 10.30am to 01.00pm\n\nDr. Abbas Chopdawala\nDNB (Med)\nOPD Timing: Fri – 10.30am to 01.00pm, Sat – 02.00pm to 04.30pm\n\nDr. Abhijit Joshi\nDiploma in Orthopaedics, Fellowship in Diabetic Foot\nOPD Timing: Mon & Wed – 02.00pm to 4.30pm\n\n");
    }

}
