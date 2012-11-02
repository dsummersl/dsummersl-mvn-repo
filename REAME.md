
To deploy to this repository:

1. Checkout this repository in your local filesystem.
2. Go to your maven project, and modify pom.xml

    <distributionManagement>
        <repository>
            <id>repo</id>
            <url>https://github.com/dsummersl/dsummersl-mvn-repo/raw/master/releases</url>
        </repository>
        <snapshotRepository>
            <id>snapshot-repo</id>
            <url>https://github.com/dsummersl/dsummersl-mvn-repo/raw/master/snapshots</url>
        </snapshotRepository>
    </distributionManagement>

3. Go to your maven project and run the following command to deploy:

    mvn -DaltDeploymentRepository=snapshot-repo::default::file:<path to project dsummersl-mvn-repo>/snapshots

4. Commit the new resources.
