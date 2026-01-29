# Hospital_Management
#It is developed by java based system for patient insurance management

Conversation opened. 1 unread message.

Skip to content
Using Gmail with screen readers
1 of 1,638
(no subject)
Inbox

Arunkumar V <arunkumarveera2004@gmail.com>
14:59 (0 minutes ago)
to me


class Patient {
    String name;
    int age;
    String hospitalId;
    String disease;
    double treatmentCost;
    void setPatientDetails(String name, int age, String hospitalId, String disease, double treatmentCost) {
        this.name = name;
        this.age = age;
        this.hospitalId = hospitalId;
        this.disease = disease;
        this.treatmentCost = treatmentCost;
    }
    void performDuty() {
        System.out.println("Follow health protocols.");
    }
    void accessCityService() {
        System.out.println("Accessing hospital and treatment services.");
    }
    void displayPatientInfo() {
        System.out.println("\n--- Patient Details ---");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Hospital ID: " + hospitalId);
        System.out.println("Disease: " + disease);
        System.out.println("Treatment Cost: Rs" + treatmentCost);
    }
}
class InsuredPatient extends Patient {
    String insuranceProvider;
    double claimAmount;
    void setInsuranceDetails(String insuranceProvider, double claimAmount) {
        this.insuranceProvider = insuranceProvider;
        this.claimAmount = claimAmount;
    }
    void accessCityService() {
        System.out.println("Accessing hospital and treatment services.");
        System.out.println("Accessing Insurance claim portal: " + insuranceProvider);
    }
    void displayInsuranceInfo() {
        System.out.println("\n--- Insurance Details ---");
        System.out.println("Insurance Provider: " + insuranceProvider);
        System.out.println("Claim Amount: Rs" + claimAmount);
    }
    public static void main(String[] args) {
        InsuredPatient ip = new InsuredPatient();
        ip.setPatientDetails("Diya", 20, "HOSP123", "Heart disease", 500000);
        ip.setInsuranceDetails("LIC Health", 450000);
        ip.displayPatientInfo();
        ip.displayInsuranceInfo();
        ip.performDuty();
        ip.accessCityService();
    }
}


