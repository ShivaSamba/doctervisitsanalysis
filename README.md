import java.util.ArrayList;
import java.util.List;

class DoctorVisit {
    private String patientName;
    private int visitDuration;

    public DoctorVisit(String patientName, int visitDuration) {
        this.patientName = patientName;
        this.visitDuration = visitDuration;
    }

    public String getPatientName() {
        return patientName;
    }

    public int getVisitDuration() {
        return visitDuration;
    }
}

public class DoctorVisitsAnalysis {

    public static void main(String[] args) {
        // Sample doctor visits data (patientName, visitDuration in minutes)
        List<DoctorVisit> doctorVisits = new ArrayList<>();
        doctorVisits.add(new DoctorVisit("John Doe", 30));
        doctorVisits.add(new DoctorVisit("Jane Smith", 45));
        doctorVisits.add(new DoctorVisit("Michael Johnson", 20));
        doctorVisits.add(new DoctorVisit("Emily Brown", 60));
        doctorVisits.add(new DoctorVisit("David Lee", 15));

        // Calculate the average duration of doctor visits
        double totalDuration = 0;
        for (DoctorVisit visit : doctorVisits) {
            totalDuration += visit.getVisitDuration();
        }

        double averageDuration = totalDuration / doctorVisits.size();

        System.out.println("Average duration of doctor visits: " + averageDuration + " minutes.");
    }
}
