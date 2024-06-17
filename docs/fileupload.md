
## Browser File Uploads

Go ahead and login and click the "File Broswer" in the top right. You will be able to drag and drop. However, be warned that you cannot upload files directly to the root of your user. You will need to make a new folder first. 

## Bulk Uploads

Bulk data uploads with sftp and ftp are available for collaborators, see the details below. 

**NOTE: This is currently in beta and not all accounts are activated on the SFTP server. **

Additionally, if you have tons of data you want to analyze in GNPS2, we'd recommend making a public dataset at MassIVE and then utilizing USIs to select that data for analysis in GNPS2. 

### SFTP File Uploads

You can access the SFTP file upload with the following information

| Field | Value | 
| ----- | ----- |
| hostname | sftp.gnps2.org |
| port | 6542 |

You can login with your GNPS2 username and password. 

Here is a one-liner if you like using the commandline for uploading a folder

```
sftp -P 6542 <username>@sftp.gnps2.org:/ <<< $'put -r <folder name>'
```

If you want to mirror a lot of data periodically, use this command:

```
lftp -e "mirror --parallel=4 --include '/*.mzML' -R $local_directory $remote_directory; quit" -u "$remote_user,$password" sftp://$remote_host:$remote_port
```

### FTP File Uploads

If you want to upload with FTP because SFTP is blocked or has issues at your institution or computer, you can use the following information

| Field | Value | 
| ----- | ----- |
| hostname | ftp.gnps2.org |
| port | 6541 |

