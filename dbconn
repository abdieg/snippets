import java.sql.*;

public class OracleDatabaseDriver {

private String url;
private String username;
private String password;

private Connection connection;

public OracleDatabaseDriver(String url, String username, String password){
    this.url = url;
    this.username = username;
    this.password = password;
}

public void openConnection() throws SQLException{
    this.connection =  DriverManager.getConnection(this.url, this.username, this.password);
}

public void closeConnection() throws SQLException{
    if(this.connection != null){
        this.connection.close();
    }
}

public void executeUpdateQuery(String query) throws SQLException {
    Statement stmt =  connection.createStatement();
    stmt.executeUpdate(query);
}

public ResultSet executeQuery(String query) throws SQLException {
    Statement stmt =  connection.createStatement();
    return stmt.executeQuery(query);
}

}
