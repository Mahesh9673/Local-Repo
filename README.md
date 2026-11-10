# This is my Local Repo.


2026-11-10 12:14:53
Full thread dump Java HotSpot(TM) 64-Bit Server VM (25.461-b11 mixed mode):

"Thread-2662795" #2942869 prio=5 os_prio=0 tid=0x00007f1a1ddfc000 nid=0x13797 runnable [0x00007f19afbfd000]
   java.lang.Thread.State: RUNNABLE
	at sun.nio.ch.FileDispatcherImpl.read0(Native Method)
	at sun.nio.ch.SocketDispatcher.read(SocketDispatcher.java:39)
	at sun.nio.ch.IOUtil.readIntoNativeBuffer(IOUtil.java:223)
	at sun.nio.ch.IOUtil.read(IOUtil.java:197)
	at sun.nio.ch.SocketChannelImpl.read(SocketChannelImpl.java:378)
	- locked <0x00000004d24f7588> (a java.lang.Object)
	at oracle.net.nt.TimeoutSocketChannel.read(TimeoutSocketChannel.java:144)
	at oracle.net.ns.NIOHeader.readHeaderBuffer(NIOHeader.java:82)
	at oracle.net.ns.NIOPacket.readFromSocketChannel(NIOPacket.java:139)
	at oracle.net.ns.NIOPacket.readFromSocketChannel(NIOPacket.java:101)
	at oracle.net.ns.NIONSDataChannel.readDataFromSocketChannel(NIONSDataChannel.java:80)
	at oracle.jdbc.driver.T4CMAREngineNIO.prepareForReading(T4CMAREngineNIO.java:98)
	at oracle.jdbc.driver.T4CMAREngineNIO.unmarshalUB1(T4CMAREngineNIO.java:534)
	at oracle.jdbc.driver.T4CTTIfun.receive(T4CTTIfun.java:485)
	at oracle.jdbc.driver.T4CTTIfun.doRPC(T4CTTIfun.java:252)
	at oracle.jdbc.driver.T4C8Oall.doOALL(T4C8Oall.java:612)
	at oracle.jdbc.driver.T4CCallableStatement.doOall8(T4CCallableStatement.java:223)
	at oracle.jdbc.driver.T4CCallableStatement.doOall8(T4CCallableStatement.java:56)
	at oracle.jdbc.driver.T4CCallableStatement.executeForRows(T4CCallableStatement.java:907)
	at oracle.jdbc.driver.OracleStatement.doExecuteWithTimeout(OracleStatement.java:1119)
	at oracle.jdbc.driver.OraclePreparedStatement.executeInternal(OraclePreparedStatement.java:3780)
	at oracle.jdbc.driver.T4CCallableStatement.executeInternal(T4CCallableStatement.java:1300)
	at oracle.jdbc.driver.OraclePreparedStatement.execute(OraclePreparedStatement.java:3887)
	- locked <0x00000004d24f4180> (a oracle.jdbc.driver.T4CConnection)
	at oracle.jdbc.driver.OracleCallableStatement.execute(OracleCallableStatement.java:4230)
	- locked <0x00000004d24f4180> (a oracle.jdbc.driver.T4CConnection)
	at oracle.jdbc.driver.OraclePreparedStatementWrapper.execute(OraclePreparedStatementWrapper.java:1079)
	at sun.reflect.GeneratedMethodAccessor61.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at oracle.ucp.jdbc.proxy.StatementProxyFactory.invoke(StatementProxyFactory.java:367)
	at com.sun.proxy.$Proxy24.execute(Unknown Source)
	at com.sbi.whatsapp.processor.WhatsAppDaoProcessor.wapp_reqMsgInsertionNew(WhatsAppDaoProcessor.java:1873)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:195)
	- locked <0x00000006cb07c520> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662794" #2942868 prio=5 os_prio=0 tid=0x00007f1a1ed28800 nid=0x13795 runnable [0x00007f19b7cfe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006cb066378> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006cb05cab8> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006cb05cab8> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.getCBSMobileNoWithISDCode(EISServices.java:242)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:216)
	- locked <0x00000006cafc8548> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f54b8d58> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662793" #2942867 prio=5 os_prio=0 tid=0x00007f1a1ee15000 nid=0x13790 runnable [0x00007f19b41fd000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006caf511c8> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006caf47908> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006caf47908> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.getCBSMobileNoWithISDCode(EISServices.java:242)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:216)
	- locked <0x00000006caf0f4a0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000006cea4b1d8> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662792" #2942866 prio=5 os_prio=0 tid=0x00007f1a1ddef000 nid=0x13789 runnable [0x00007f19be2fe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006cae37ff0> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006cae2e748> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006cae2e748> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.getCBSMobileNoWithISDCode(EISServices.java:242)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:216)
	- locked <0x00000006cad9cb08> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f53a40a8> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Attach Listener" #2942865 daemon prio=9 os_prio=0 tid=0x00007f1914001800 nid=0x13776 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"Thread-2662791" #2942864 prio=5 os_prio=0 tid=0x00007f1a1c6c6800 nid=0x13772 runnable [0x00007f19be1fe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006cad67de8> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006cad5e528> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006cad5e528> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.getCBSMobileNoWithISDCode(EISServices.java:242)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:216)
	- locked <0x00000006caa8e1e8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000006c8a8b6a0> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662790" #2942863 prio=5 os_prio=0 tid=0x00007f1a1ed2c800 nid=0x13753 runnable [0x00007f19be6fe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006cafadda8> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006cafa4238> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006cafa4238> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.cifServiceCall(EISServices.java:362)
	at com.sbi.whatsapp.eisg6.service.balance_enquiry.BalanceEnquiryRevised.balanceService(BalanceEnquiryRevised.java:56)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:355)
	- locked <0x00000006ca7603d0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000006c8ae5ea8> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662789" #2942862 prio=5 os_prio=0 tid=0x00007f1a1c0cf800 nid=0x1374b waiting on condition [0x00007f19beefe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ca842e48> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ca6f3c58> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662788" #2942861 prio=5 os_prio=0 tid=0x00007f1a1e9ac800 nid=0x13735 runnable [0x00007f19c41fe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006caef69d8> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006caeecfe0> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006caeecfe0> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.cifServiceCall(EISServices.java:362)
	at com.sbi.whatsapp.eis.statements.MiniStatementAck.miniStmtServiceAck(MiniStatementAck.java:53)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:368)
	- locked <0x00000006ca64c398> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000006ceac3c18> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662787" #2942860 prio=5 os_prio=0 tid=0x00007f1a1cb51800 nid=0x13731 waiting on condition [0x00007f19bd5fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ca5d8468> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ca538678> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662786" #2942859 prio=5 os_prio=0 tid=0x00007f1a1de06800 nid=0x13725 waiting on condition [0x00007f19bd3fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ca7bd000> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ca2b00a0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662785" #2942858 prio=5 os_prio=0 tid=0x00007f1a1dad4000 nid=0x13721 runnable [0x00007f19bcffe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006ca985d40> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006ca97c318> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006ca97c318> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.cifServiceCall(EISServices.java:362)
	at com.sbi.whatsapp.eisg6.service.balance_enquiry.BalanceEnquiryRevised.balanceService(BalanceEnquiryRevised.java:56)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:355)
	- locked <0x00000006ca1af098> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000006ceafb8f0> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662784" #2942857 prio=5 os_prio=0 tid=0x00007f1a1ca75000 nid=0x1371b runnable [0x00007f19bddfe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006ca91c768> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006ca912c08> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006ca912c08> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.EISServices.cifServiceCall(EISServices.java:362)
	at com.sbi.whatsapp.eisg6.service.balance_enquiry.BalanceEnquiryRevised.balanceService(BalanceEnquiryRevised.java:56)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:355)
	- locked <0x00000006ca17b8b8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f54fdf68> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662783" #2942856 prio=5 os_prio=0 tid=0x00007f1a1cb4e000 nid=0x1370e waiting on condition [0x00007f19bdbfe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c9fc68f0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c9ed18c8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662782" #2942855 prio=5 os_prio=0 tid=0x00007f1a1d21e000 nid=0x13700 runnable [0x00007f19b7efd000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006caeb1dd8> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006caea8310> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006caea8310> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eisg6.EISEnquiryServiceGen6.callEISService(EISEnquiryServiceGen6.java:47)
	at com.sbi.whatsapp.eisg6.EISServicesGen6.isKycCompliant(EISServicesGen6.java:233)
	at com.sbi.whatsapp.eis.newregistration.NewRegistrationUtility.isKycCompliantCommon(NewRegistrationUtility.java:123)
	at com.sbi.whatsapp.eis.newregistration.NewRegistrationStep1.validateAllCifLeveleChecks(NewRegistrationStep1.java:90)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:323)
	- locked <0x00000006c9bc8700> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f5493a00> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662781" #2942854 prio=5 os_prio=0 tid=0x00007f1a1e9b3800 nid=0x136fc waiting on condition [0x00007f1a208fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006cae0b618> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c991bac0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662780" #2942853 prio=5 os_prio=0 tid=0x00007f1a1cb10800 nid=0x136ef waiting on condition [0x00007f19bdefe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c9dd5e40> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c95fd450> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662779" #2942852 prio=5 os_prio=0 tid=0x00007f1a1cb50800 nid=0x136ea runnable [0x00007f19bdcfe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006caa76330> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006caa6cb20> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006caa6cb20> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eis.EISEnquiryService.callEISService(EISEnquiryService.java:41)
	at com.sbi.whatsapp.eis.statements.MiniStatementAck.generateMiniStatement(MiniStatementAck.java:137)
	at com.sbi.whatsapp.eis.statements.MiniStatementAck.miniStmtServiceAck(MiniStatementAck.java:83)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:368)
	- locked <0x00000006c95c8d48> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f530d0e0> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662778" #2942851 prio=5 os_prio=0 tid=0x00007f1a1ed19000 nid=0x136df waiting on condition [0x00007f19bdafe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c943a800> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c92ff128> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662777" #2942850 prio=5 os_prio=0 tid=0x00007f1a1cb1a800 nid=0x136d7 waiting on condition [0x00007f19b7dfe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c96b6d90> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c912b700> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662776" #2942849 prio=5 os_prio=0 tid=0x00007f1a1ed23000 nid=0x136cf waiting on condition [0x00007f19b5ffd000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006cb03e090> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c8f2f998> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662775" #2942848 prio=5 os_prio=0 tid=0x00007f1a1cb19800 nid=0x136cb waiting on condition [0x00007f1a205fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c8fd5738> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c8eabf40> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662774" #2942845 prio=5 os_prio=0 tid=0x00007f1a1c092000 nid=0x136c1 runnable [0x00007f19b52fc000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at java.io.BufferedInputStream.fill(BufferedInputStream.java:246)
	at java.io.BufferedInputStream.read1(BufferedInputStream.java:286)
	at java.io.BufferedInputStream.read(BufferedInputStream.java:345)
	- locked <0x00000006ca28cca8> (a java.io.BufferedInputStream)
	at sun.net.www.http.HttpClient.parseHTTPHeader(HttpClient.java:779)
	at sun.net.www.http.HttpClient.parseHTTP(HttpClient.java:714)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1646)
	- locked <0x00000006ca282ff0> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1551)
	- locked <0x00000006ca282ff0> (a sun.net.www.protocol.https.DelegateHttpsURLConnection)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:480)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:352)
	at com.sbi.whatsapp.eis.WSClientURLProcessImpl.processRequest(WSClientURLProcessImpl.java:59)
	at com.sbi.whatsapp.eisg6.EISEnquiryServiceGen6.callEISService(EISEnquiryServiceGen6.java:47)
	at com.sbi.whatsapp.eis.service.kyc.KycUpdateStep3Ack.invokeKYCReqeust(KycUpdateStep3Ack.java:266)
	at com.sbi.whatsapp.eis.service.kyc.KycUpdateStep3Ack.updateKycStep3Ack(KycUpdateStep3Ack.java:116)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:437)
	- locked <0x00000006c8aaaed0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f53c41f0> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662773" #2942844 prio=5 os_prio=0 tid=0x00007f1a1cb5e800 nid=0x136bd waiting on condition [0x00007f19bdffe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ca966868> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c89efa30> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662772" #2942843 prio=5 os_prio=0 tid=0x00007f1a1de00000 nid=0x136b9 waiting on condition [0x00007f19b66fd000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ca445810> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c88c5798> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662771" #2942842 prio=5 os_prio=0 tid=0x00007f1a1cc12000 nid=0x136a6 waiting on condition [0x00007f19be9fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c8e780b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c87a7e60> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662770" #2942841 prio=5 os_prio=0 tid=0x00007f1a1da74800 nid=0x136a0 waiting on condition [0x00007f19be7fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ca1618b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c86110d0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662769" #2942840 prio=5 os_prio=0 tid=0x00007f1a1dde9800 nid=0x1369b waiting on condition [0x00007f19bf8fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c9b593a0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c84c3070> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662768" #2942839 prio=5 os_prio=0 tid=0x00007f1a1cc50000 nid=0x13699 waiting on condition [0x00007f19bedfe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c92f3a90> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c847dfe8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662767" #2942838 prio=5 os_prio=0 tid=0x00007f1a1eeab000 nid=0x13686 waiting on condition [0x00007f19afcfe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c8670ef0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c82359a0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662766" #2942837 prio=5 os_prio=0 tid=0x00007f1a1de94800 nid=0x1367b waiting on condition [0x00007f19c44fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c974b8a8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c8138258> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662765" #2942836 prio=5 os_prio=0 tid=0x00007f1a1ee17000 nid=0x1367a waiting on condition [0x00007f19bf7fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c8bb39b0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c8103060> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662764" #2942835 prio=5 os_prio=0 tid=0x00007f1a1ed1b000 nid=0x13667 waiting on condition [0x00007f19becfe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c835fc38> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c7e56468> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662763" #2942834 prio=5 os_prio=0 tid=0x00007f1a1de2e000 nid=0x13661 waiting on condition [0x00007f19bcafe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c82ed058> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c7e34c60> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662762" #2942833 prio=5 os_prio=0 tid=0x00007f1a1c45e000 nid=0x1365b waiting on condition [0x00007f19c56fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c808f060> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c7d0f998> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662761" #2942832 prio=5 os_prio=0 tid=0x00007f1a1c44d800 nid=0x1364f waiting on condition [0x00007f19bc1fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c84302f0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c7887f78> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662760" #2942831 prio=5 os_prio=0 tid=0x00007f1a1e9b1800 nid=0x13648 waiting on condition [0x00007f19beffe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c8d39790> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c78430b8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662759" #2942830 prio=5 os_prio=0 tid=0x00007f1a1ed0f000 nid=0x1363f waiting on condition [0x00007f19c40fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c8e29fc8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c76b6588> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662758" #2942829 prio=5 os_prio=0 tid=0x00007f1a1eeee000 nid=0x1362e waiting on condition [0x00007f19b6dfd000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c7923a50> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c7373c20> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662757" #2942828 prio=5 os_prio=0 tid=0x00007f1a1ccad000 nid=0x13628 waiting on condition [0x00007f19be4fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c7f19388> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c72df968> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662756" #2942827 prio=5 os_prio=0 tid=0x00007f1a1da72800 nid=0x1361f waiting on condition [0x00007f19c4efe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c7731788> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c71a82b0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662755" #2942826 prio=5 os_prio=0 tid=0x00007f1a1c465800 nid=0x13616 waiting on condition [0x00007f1a207fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c76785b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c6fe2eb0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662754" #2942825 prio=5 os_prio=0 tid=0x00007f1a1ee13000 nid=0x13610 waiting on condition [0x00007f19c67fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c755d360> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c6dcf0f8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662753" #2942824 prio=5 os_prio=0 tid=0x00007f1a1da93000 nid=0x1360a waiting on condition [0x00007f19be5fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c6e2aa28> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c6c848d8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662752" #2942823 prio=5 os_prio=0 tid=0x00007f1a1da95000 nid=0x13600 waiting on condition [0x00007f19bd7fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c7367dd8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c6bc7ec8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662751" #2942822 prio=5 os_prio=0 tid=0x00007f1a1eea9000 nid=0x135f6 waiting on condition [0x00007f19b7ffe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c6f21f70> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c680e390> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662750" #2942821 prio=5 os_prio=0 tid=0x00007f1a1ca93000 nid=0x135f5 waiting on condition [0x00007f19bf2fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c6f90f78> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c67aef60> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662749" #2942820 prio=5 os_prio=0 tid=0x00007f1a1c70a000 nid=0x135eb waiting on condition [0x00007f19bf3fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c6d58f58> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c655b690> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662748" #2942819 prio=5 os_prio=0 tid=0x00007f1a1c72e000 nid=0x135ea waiting on condition [0x00007f19b70fd000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c666f1c0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c6526498> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662747" #2942818 prio=5 os_prio=0 tid=0x00007f1a1ece5800 nid=0x135e0 waiting on condition [0x00007f19bf9fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c859dfd8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006c62e9a60> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662746" #2942817 prio=5 os_prio=0 tid=0x00007f1a1dcd7000 nid=0x135d6 waiting on condition [0x00007f19be8fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c79d18c0> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8a80c8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662745" #2942816 prio=5 os_prio=0 tid=0x00007f1a1c6e1000 nid=0x135d3 waiting on condition [0x00007f19bf6fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c77c95d8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8b05a0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662744" #2942815 prio=5 os_prio=0 tid=0x00007f1a1da89800 nid=0x135ca waiting on condition [0x00007f19bd9fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ce8a3eb8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8b8210> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662743" #2942814 prio=5 os_prio=0 tid=0x00007f1a1c731000 nid=0x135c8 waiting on condition [0x00007f1a209fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c64cb6d8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8c2300> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662742" #2942813 prio=5 os_prio=0 tid=0x00007f1a1ed15800 nid=0x135c0 waiting on condition [0x00007f1a206fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c6b160a8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8aa6c8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662741" #2942812 prio=5 os_prio=0 tid=0x00007f1a1c6dc800 nid=0x135bd waiting on condition [0x00007f19c45fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c88ac660> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8c85b8> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662739" #2942810 prio=5 os_prio=0 tid=0x00007f1a1de28000 nid=0x1359a waiting on condition [0x00007f19bd1fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ce8b0828> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8b0a68> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662738" #2942809 prio=5 os_prio=0 tid=0x00007f1a1de6d000 nid=0x13595 waiting on condition [0x00007f19b42fd000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c69f1e18> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8cc038> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662735" #2942805 prio=5 os_prio=0 tid=0x00007f1a1de98000 nid=0x13580 waiting on condition [0x00007f19bd2fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c74a54c8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8f2440> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662734" #2942804 prio=5 os_prio=0 tid=0x00007f1a1cc4e800 nid=0x1357c waiting on condition [0x00007f19bd4fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c6450a88> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce902368> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662732" #2942802 prio=5 os_prio=0 tid=0x00007f1a1ee05800 nid=0x1356e waiting on condition [0x00007f19bd6fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c66cf0e8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce9191b0> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662731" #2942801 prio=5 os_prio=0 tid=0x00007f1a1c09a800 nid=0x13569 waiting on condition [0x00007f19bd8fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006ce8c5810> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000006ce8c5a50> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Thread-2662726" #2942796 prio=5 os_prio=0 tid=0x00007f1a1ddf4800 nid=0x1353d runnable [0x00007f19be0fd000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at org.apache.http.impl.io.SessionInputBufferImpl.streamRead(SessionInputBufferImpl.java:139)
	at org.apache.http.impl.io.SessionInputBufferImpl.fillBuffer(SessionInputBufferImpl.java:155)
	at org.apache.http.impl.io.SessionInputBufferImpl.readLine(SessionInputBufferImpl.java:284)
	at org.apache.http.impl.conn.DefaultHttpResponseParser.parseHead(DefaultHttpResponseParser.java:140)
	at org.apache.http.impl.conn.DefaultHttpResponseParser.parseHead(DefaultHttpResponseParser.java:57)
	at org.apache.http.impl.io.AbstractMessageParser.parse(AbstractMessageParser.java:261)
	at org.apache.http.impl.DefaultBHttpClientConnection.receiveResponseHeader(DefaultBHttpClientConnection.java:165)
	at org.apache.http.impl.conn.CPoolProxy.receiveResponseHeader(CPoolProxy.java:167)
	at org.apache.http.protocol.HttpRequestExecutor.doReceiveResponse(HttpRequestExecutor.java:272)
	at org.apache.http.protocol.HttpRequestExecutor.execute(HttpRequestExecutor.java:124)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:271)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.karixClientCallConnection(KarixConnect.java:373)
	at com.sbi.whatsapp.service.KarixConnect.callkarixMediaIdService(KarixConnect.java:336)
	at com.sbi.whatsapp.eis.statements.StatementServiceForDepositPDF.depositAccntStmtPdfGeneration(StatementServiceForDepositPDF.java:323)
	at com.sbi.whatsapp.eis.statements.StatementServiceForDepositPDF.depositStmtPdfCall(StatementServiceForDepositPDF.java:112)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:482)
	- locked <0x00000006ce931b80> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- <0x00000004f4f22910> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"Thread-2662669" #2942729 prio=5 os_prio=0 tid=0x00007f1a1cb61000 nid=0x1334e waiting on condition [0x00007f19c4ffe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000006c90d6670> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at org.apache.http.pool.PoolEntryFuture.await(PoolEntryFuture.java:138)
	at org.apache.http.pool.AbstractConnPool.getPoolEntryBlocking(AbstractConnPool.java:306)
	at org.apache.http.pool.AbstractConnPool.access$000(AbstractConnPool.java:64)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:192)
	at org.apache.http.pool.AbstractConnPool$2.getPoolEntry(AbstractConnPool.java:185)
	at org.apache.http.pool.PoolEntryFuture.get(PoolEntryFuture.java:107)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.leaseConnection(PoolingHttpClientConnectionManager.java:276)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager$1.get(PoolingHttpClientConnectionManager.java:263)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:190)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000004f54d9038> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Keep-Alive-Timer" #2819837 daemon prio=8 os_prio=0 tid=0x00007f180004d000 nid=0x33f30d waiting on condition [0x00007f19bcefe000]
   java.lang.Thread.State: TIMED_WAITING (sleeping)
	at java.lang.Thread.sleep(Native Method)
	at sun.net.www.http.KeepAliveCache.run(KeepAliveCache.java:235)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Timer-1126" #2753146 daemon prio=5 os_prio=0 tid=0x00007f172c06c000 nid=0x29874f in Object.wait() [0x00007f19c50fe000]
   java.lang.Thread.State: TIMED_WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at java.util.TimerThread.mainLoop(Timer.java:552)
	- locked <0x00000004d388b8a0> (a java.util.TaskQueue)
	at java.util.TimerThread.run(Timer.java:505)

   Locked ownable synchronizers:
	- None

"Thread-1767759" #1973257 prio=5 os_prio=0 tid=0x00007f1a1c6d5000 nid=0x15c37b runnable [0x00007f19aeefd000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readFully(SSLSocketInputRecord.java:458)
	at sun.security.ssl.SSLSocketInputRecord.decodeInputRecord(SSLSocketInputRecord.java:242)
	at sun.security.ssl.SSLSocketInputRecord.decode(SSLSocketInputRecord.java:180)
	at sun.security.ssl.SSLTransport.decode(SSLTransport.java:111)
	at sun.security.ssl.SSLSocketImpl.decode(SSLSocketImpl.java:1382)
	at sun.security.ssl.SSLSocketImpl.readHandshakeRecord(SSLSocketImpl.java:1295)
	at sun.security.ssl.SSLSocketImpl.startHandshake(SSLSocketImpl.java:417)
	- locked <0x00000004d3775380> (a sun.security.ssl.TransportContext)
	at sun.security.ssl.SSLSocketImpl.startHandshake(SSLSocketImpl.java:389)
	at org.apache.http.conn.ssl.SSLConnectionSocketFactory.createLayeredSocket(SSLConnectionSocketFactory.java:394)
	at org.apache.http.impl.conn.DefaultHttpClientConnectionOperator.upgrade(DefaultHttpClientConnectionOperator.java:192)
	at org.apache.http.impl.conn.PoolingHttpClientConnectionManager.upgrade(PoolingHttpClientConnectionManager.java:369)
	at org.apache.http.impl.execchain.MainClientExec.establishRoute(MainClientExec.java:415)
	at org.apache.http.impl.execchain.MainClientExec.execute(MainClientExec.java:236)
	at org.apache.http.impl.execchain.ProtocolExec.execute(ProtocolExec.java:184)
	at org.apache.http.impl.execchain.RetryExec.execute(RetryExec.java:88)
	at org.apache.http.impl.execchain.RedirectExec.execute(RedirectExec.java:110)
	at org.apache.http.impl.client.InternalHttpClient.doExecute(InternalHttpClient.java:184)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:82)
	at org.apache.http.impl.client.CloseableHttpClient.execute(CloseableHttpClient.java:107)
	at com.sbi.whatsapp.service.KarixConnect.makeHTTPConnectionPoolRequest(KarixConnect.java:254)
	at com.sbi.whatsapp.service.KarixConnect.callkarixService(KarixConnect.java:101)
	at com.sbi.whatsapp.processor.WhatsAppProcessExecuter.receiveSMSText(WhatsAppProcessExecuter.java:2231)
	- locked <0x00000004d376cb88> (a com.sbi.whatsapp.processor.WhatsAppProcessExecuter)
	at executor.ReceiveWhatsAppThread.run(ReceiveWhatsAppThread.java:29)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Keep-Alive-SocketCleaner" #1223102 daemon prio=8 os_prio=0 tid=0x00007f1764030000 nid=0x3c27be in Object.wait() [0x00007f19bd0fe000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at sun.net.www.http.KeepAliveStreamCleaner.run(KeepAliveStreamCleaner.java:101)
	- locked <0x00000004d2a769c8> (a sun.net.www.http.KeepAliveStreamCleaner)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"oneagent-httpUrlConnection" #41 daemon prio=5 os_prio=0 tid=0x00007f18a420a800 nid=0x3030ff runnable [0x00007f19c51fe000]
   java.lang.Thread.State: TIMED_WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000004d2c1cc00> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.parkNanos(LockSupport.java:215)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.awaitNanos(AbstractQueuedSynchronizer.java:2078)
	at java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:1093)
	at java.util.concurrent.ScheduledThreadPoolExecutor$DelayedWorkQueue.take(ScheduledThreadPoolExecutor.java:809)
	at java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"RcvThread: com.ibm.mq.jmqi.remote.impl.RemoteTCPConnection@554146322[qmid=SBIWAPR4_2024-08-02_16.49.12,fap=15,channel=WAPPS.SVRCONN       ,ccsid=1208,sharecnv=10,hbint=300,peer=whatsapp.utiltomq4.sbi/10.191.64.103(4466),localport=44513,ssl=TLS_AES_256_GCM_SHA384,peerDN="CN=inbwhatsapprod.sbi, C=IN, O=SBI",issuerDN="CN=SBI-CA, C=IN, O=SBI, OU=PE-III, OID.2.5.4.17=400614, ST=Maharashtra"]" #39 daemon prio=5 os_prio=0 tid=0x00007f18ac00f800 nid=0x3030e0 runnable [0x00007f19c57fe000]
   java.lang.Thread.State: RUNNABLE
	at java.net.SocketInputStream.socketRead0(Native Method)
	at java.net.SocketInputStream.socketRead(SocketInputStream.java:116)
	at java.net.SocketInputStream.read(SocketInputStream.java:171)
	at java.net.SocketInputStream.read(SocketInputStream.java:141)
	at sun.security.ssl.SSLSocketInputRecord.read(SSLSocketInputRecord.java:475)
	at sun.security.ssl.SSLSocketInputRecord.readHeader(SSLSocketInputRecord.java:469)
	at sun.security.ssl.SSLSocketInputRecord.bytesInCompletePacket(SSLSocketInputRecord.java:69)
	at sun.security.ssl.SSLSocketImpl.readApplicationRecord(SSLSocketImpl.java:1333)
	at sun.security.ssl.SSLSocketImpl.access$300(SSLSocketImpl.java:76)
	at sun.security.ssl.SSLSocketImpl$AppInputStream.read(SSLSocketImpl.java:979)
	at com.ibm.mq.jmqi.remote.impl.RemoteTCPConnection.receive(RemoteTCPConnection.java:2046)
	at com.ibm.mq.jmqi.remote.impl.RemoteRcvThread.receiveBuffer(RemoteRcvThread.java:833)
	at com.ibm.mq.jmqi.remote.impl.RemoteRcvThread.receiveOneTSH(RemoteRcvThread.java:798)
	at com.ibm.mq.jmqi.remote.impl.RemoteRcvThread.run(RemoteRcvThread.java:161)
	at com.ibm.msg.client.commonservices.workqueue.WorkQueueItem.runTask(WorkQueueItem.java:319)
	at com.ibm.msg.client.commonservices.workqueue.SimpleWorkQueueItem.runItem(SimpleWorkQueueItem.java:99)
	at com.ibm.msg.client.commonservices.workqueue.WorkQueueItem.run(WorkQueueItem.java:343)
	at com.ibm.msg.client.commonservices.workqueue.WorkQueueManager.runWorkQueueItem(WorkQueueManager.java:312)
	at com.ibm.msg.client.commonservices.j2se.workqueue.WorkQueueManagerImplementation$ThreadPoolWorker.run(WorkQueueManagerImplementation.java:1240)

   Locked ownable synchronizers:
	- <0x00000004d2d7a400> (a java.util.concurrent.locks.ReentrantLock$NonfairSync)

"JMSCCThreadPoolMaster" #38 daemon prio=5 os_prio=0 tid=0x00007f1a1ecdb000 nid=0x3030df in Object.wait() [0x00007f19c5efe000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at java.lang.Object.wait(Object.java:502)
	at com.ibm.msg.client.commonservices.j2se.workqueue.WorkQueueManagerImplementation$WorkQueueManagerThread.waitForNotification(WorkQueueManagerImplementation.java:678)
	- locked <0x00000004d2bef000> (a java.lang.Object)
	at com.ibm.msg.client.commonservices.j2se.workqueue.WorkQueueManagerImplementation$WorkQueueManagerThread.waitForNotification(WorkQueueManagerImplementation.java:648)
	at com.ibm.msg.client.commonservices.j2se.workqueue.WorkQueueManagerImplementation$WorkQueueManagerThread.run(WorkQueueManagerImplementation.java:918)

   Locked ownable synchronizers:
	- None

"PoolScavenger0" #36 daemon prio=5 os_prio=0 tid=0x00007f1a1e8a8000 nid=0x3030d1 in Object.wait() [0x00007f19c5ffe000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at java.lang.Object.wait(Object.java:502)
	at com.ibm.mq.PoolScavenger.run(PoolScavenger.java:173)
	- locked <0x00000004d252a078> (a java.lang.Object)
	- locked <0x00000004d2529f90> (a com.ibm.mq.PoolScavenger)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"UCP-worker-thread-4" #35 daemon prio=5 os_prio=0 tid=0x00007f1a1e86f000 nid=0x3030c2 waiting on condition [0x00007f19c64fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000004d215b4b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at java.util.concurrent.ArrayBlockingQueue.take(ArrayBlockingQueue.java:403)
	at java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"UCP-worker-thread-3" #34 daemon prio=5 os_prio=0 tid=0x00007f1a1e8ca000 nid=0x3030c1 waiting on condition [0x00007f19c65fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000004d215b4b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at java.util.concurrent.ArrayBlockingQueue.take(ArrayBlockingQueue.java:403)
	at java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"UCP-worker-thread-2" #33 daemon prio=5 os_prio=0 tid=0x00007f1a1e832000 nid=0x3030c0 waiting on condition [0x00007f19c66fe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000004d215b4b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at java.util.concurrent.ArrayBlockingQueue.take(ArrayBlockingQueue.java:403)
	at java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"UCP-worker-thread-1" #31 daemon prio=5 os_prio=0 tid=0x00007f18c4003800 nid=0x3030ab waiting on condition [0x00007f19c6afe000]
   java.lang.Thread.State: WAITING (parking)
	at sun.misc.Unsafe.park(Native Method)
	- parking to wait for  <0x00000004d215b4b8> (a java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject)
	at java.util.concurrent.locks.LockSupport.park(LockSupport.java:175)
	at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.await(AbstractQueuedSynchronizer.java:2039)
	at java.util.concurrent.ArrayBlockingQueue.take(ArrayBlockingQueue.java:403)
	at java.util.concurrent.ThreadPoolExecutor.getTask(ThreadPoolExecutor.java:1074)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1134)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)

   Locked ownable synchronizers:
	- None

"Timer-2" #30 daemon prio=5 os_prio=0 tid=0x00007f1a1e81f800 nid=0x3030aa in Object.wait() [0x00007f19c6bfe000]
   java.lang.Thread.State: TIMED_WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at java.util.TimerThread.mainLoop(Timer.java:552)
	- locked <0x00000004d232e478> (a java.util.TaskQueue)
	at java.util.TimerThread.run(Timer.java:505)

   Locked ownable synchronizers:
	- None

"InterruptTimer" #28 daemon prio=5 os_prio=0 tid=0x00007f1a1e3cd000 nid=0x30308e in Object.wait() [0x00007f19c7ffe000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	- waiting on <0x00000004d235a050> (a java.util.TaskQueue)
	at java.lang.Object.wait(Object.java:502)
	at java.util.TimerThread.mainLoop(Timer.java:526)
	- locked <0x00000004d235a050> (a java.util.TaskQueue)
	at java.util.TimerThread.run(Timer.java:505)

   Locked ownable synchronizers:
	- None

"oracle.jdbc.driver.BlockSource.ThreadedCachingBlockSource.BlockReleaser" #27 daemon prio=4 os_prio=0 tid=0x00007f1a1e8aa000 nid=0x303086 in Object.wait() [0x00007f19cc15c000]
   java.lang.Thread.State: TIMED_WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at oracle.jdbc.driver.BlockSource$ThreadedCachingBlockSource$BlockReleaser.run(BlockSource.java:329)
	- locked <0x00000004d1e1bd38> (a oracle.jdbc.driver.BlockSource$ThreadedCachingBlockSource$BlockReleaser)

   Locked ownable synchronizers:
	- None

"Timer-0" #26 daemon prio=5 os_prio=0 tid=0x00007f1a1e807800 nid=0x303085 in Object.wait() [0x00007f19cc2b4000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	- waiting on <0x00000004d1e24aa0> (a java.util.TaskQueue)
	at java.lang.Object.wait(Object.java:502)
	at java.util.TimerThread.mainLoop(Timer.java:526)
	- locked <0x00000004d1e24aa0> (a java.util.TaskQueue)
	at java.util.TimerThread.run(Timer.java:505)

   Locked ownable synchronizers:
	- None

"oneagentsoftwarecomponentextraction" #23 daemon prio=5 os_prio=0 tid=0x00007f1910001800 nid=0x303052 runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"Service Thread" #22 daemon prio=9 os_prio=0 tid=0x00007f1a1da35000 nid=0x30306c runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C1 CompilerThread11" #21 daemon prio=9 os_prio=0 tid=0x00007f1a1da32800 nid=0x30306b waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C1 CompilerThread10" #20 daemon prio=9 os_prio=0 tid=0x00007f1a1da56800 nid=0x30306a waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C1 CompilerThread9" #19 daemon prio=9 os_prio=0 tid=0x00007f1a1da54800 nid=0x303069 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C1 CompilerThread8" #18 daemon prio=9 os_prio=0 tid=0x00007f1a1da52800 nid=0x303068 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread7" #17 daemon prio=9 os_prio=0 tid=0x00007f1a1da50800 nid=0x303067 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread6" #16 daemon prio=9 os_prio=0 tid=0x00007f1a1da4e800 nid=0x303066 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread5" #15 daemon prio=9 os_prio=0 tid=0x00007f1a1db81000 nid=0x303065 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread4" #14 daemon prio=9 os_prio=0 tid=0x00007f1a1db7f000 nid=0x303064 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread3" #13 daemon prio=9 os_prio=0 tid=0x00007f1a1db7d000 nid=0x303063 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread2" #12 daemon prio=9 os_prio=0 tid=0x00007f1a1d2ae000 nid=0x30305a waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread1" #11 daemon prio=9 os_prio=0 tid=0x00007f1a1d2ac000 nid=0x303059 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"C2 CompilerThread0" #10 daemon prio=9 os_prio=0 tid=0x00007f1a1db74800 nid=0x303058 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"oneagentautosensor" #9 daemon prio=5 os_prio=0 tid=0x00007f19f0001000 nid=0x302fc3 runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"oneagentperiodiceventsmanaged" #7 daemon prio=5 os_prio=0 tid=0x00007f19e4001800 nid=0x302fc4 runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"oneagentsubpathsender 1.345.93.20261023-231338" #6 daemon prio=5 os_prio=0 tid=0x00007f19ec001800 nid=0x302fb3 runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"oneagentperiodicrequests" #5 daemon prio=5 os_prio=0 tid=0x00007f1a00001800 nid=0x302fa3 runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"Signal Dispatcher" #4 daemon prio=9 os_prio=0 tid=0x00007f1a1d9f3000 nid=0x302ff6 runnable [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

   Locked ownable synchronizers:
	- None

"Finalizer" #3 daemon prio=8 os_prio=0 tid=0x00007f1a1d9b5000 nid=0x302ff4 in Object.wait() [0x00007f19cdada000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at java.lang.ref.ReferenceQueue.remove(ReferenceQueue.java:150)
	- locked <0x00000004d1e24c30> (a java.lang.ref.ReferenceQueue$Lock)
	at java.lang.ref.ReferenceQueue.remove(ReferenceQueue.java:171)
	at java.lang.ref.Finalizer$FinalizerThread.run(Finalizer.java:188)

   Locked ownable synchronizers:
	- None

"Reference Handler" #2 daemon prio=10 os_prio=0 tid=0x00007f1a1d9ac800 nid=0x302ff2 in Object.wait() [0x00007f19cdbda000]
   java.lang.Thread.State: WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at java.lang.Object.wait(Object.java:502)
	at java.lang.ref.Reference.tryHandlePending(Reference.java:191)
	- locked <0x00000004d1e22228> (a java.lang.ref.Reference$Lock)
	at java.lang.ref.Reference$ReferenceHandler.run(Reference.java:153)

   Locked ownable synchronizers:
	- None

"main" #1 prio=5 os_prio=0 tid=0x00007f1a1d092800 nid=0x302ece in Object.wait() [0x00007f1a23f21000]
   java.lang.Thread.State: TIMED_WAITING (on object monitor)
	at java.lang.Object.wait(Native Method)
	at com.ibm.mq.jmqi.remote.impl.RemoteProxyQueue.proxyMQGET(RemoteProxyQueue.java:2688)
	- locked <0x00000004d388bd20> (a com.ibm.mq.jmqi.remote.impl.RemoteProxyQueue$GetterEventMonitor)
	at com.ibm.mq.jmqi.remote.api.RemoteFAP.jmqiGetInternalWithRecon(RemoteFAP.java:6152)
	at com.ibm.mq.jmqi.remote.api.RemoteFAP.jmqiGetInternal(RemoteFAP.java:6039)
	at com.ibm.mq.jmqi.internal.JmqiTools.getMessage(JmqiTools.java:1358)
	at com.ibm.mq.jmqi.remote.api.RemoteFAP.jmqiGet(RemoteFAP.java:6002)
	at com.ibm.mq.ese.jmqi.InterceptedJmqiImpl.jmqiGet(InterceptedJmqiImpl.java:1341)
	at com.ibm.mq.ese.jmqi.ESEJMQI.jmqiGet(ESEJMQI.java:602)
	at com.ibm.mq.MQDestination.internalGetMessage(MQDestination.java:1077)
	- eliminated <0x00000004d388d900> (a com.ibm.mq.MQQueue)
	at com.ibm.mq.MQDestination.getInt(MQDestination.java:612)
	- locked <0x00000004d388d900> (a com.ibm.mq.MQQueue)
	at com.ibm.mq.MQDestination.get(MQDestination.java:452)
	at com.sbi.whatsapp.main.ValidateWhatsAppParam.messageProcessor(ValidateWhatsAppParam.java:56)
	- locked <0x00000004d1e349b8> (a com.sbi.whatsapp.main.ValidateWhatsAppParam)
	at com.sbi.whatsapp.main.ValidateWhatsAppParam.main(ValidateWhatsAppParam.java:131)

   Locked ownable synchronizers:
	- <0x00000004d282c7a0> (a java.util.concurrent.locks.ReentrantLock$FairSync)

"VM Thread" os_prio=0 tid=0x00007f1a1d6d6000 nid=0x302ff0 runnable 

"GC task thread#0 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0a5800 nid=0x302fdc runnable 

"GC task thread#1 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0a7000 nid=0x302fdd runnable 

"GC task thread#2 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0a8800 nid=0x302fde runnable 

"GC task thread#3 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0aa800 nid=0x302fdf runnable 

"GC task thread#4 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0ac000 nid=0x302fe0 runnable 

"GC task thread#5 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0ae000 nid=0x302fe1 runnable 

"GC task thread#6 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0b0000 nid=0x302fe2 runnable 

"GC task thread#7 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0b1800 nid=0x302fe3 runnable 

"GC task thread#8 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0b3800 nid=0x302fe4 runnable 

"GC task thread#9 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0b5000 nid=0x302fe5 runnable 

"GC task thread#10 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0b7000 nid=0x302fe6 runnable 

"GC task thread#11 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0b8800 nid=0x302fe7 runnable 

"GC task thread#12 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0ba800 nid=0x302fe8 runnable 

"GC task thread#13 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0bc000 nid=0x302fe9 runnable 

"GC task thread#14 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0be000 nid=0x302fea runnable 

"GC task thread#15 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0bf800 nid=0x302feb runnable 

"GC task thread#16 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0c1800 nid=0x302fec runnable 

"GC task thread#17 (ParallelGC)" os_prio=0 tid=0x00007f1a1d0c3000 nid=0x302fed runnable 

"VM Periodic Task Thread" os_prio=0 tid=0x00007f1a1da41000 nid=0x30306d waiting on condition 

JNI global references: 813

