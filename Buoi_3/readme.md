# Trình bày chi tiết về POW, POS, DPOS trong BlockChain

# Proof of Work (POW)

### `Khái niệm`

-   Proof of Work là một cơ chế đồng thuận (consensus mechanism) trong blockchain, được sử dụng để đảm bảo rằng các nút trên mạng đồng thuận về sự thay đổi của blockchain.
-   Proof of Work là một thuật toán được sử dụng để xác minh giao dịch và tạo một khối mới trong chuỗi khối.

### `Cơ chế hoạt động`

-   Khi một người dùng gửi một giao dịch trên blockchain, thì mạng sẽ phải xác nhận và chứng minh rằng giao dịch đó là hợp lệ và được chấp nhận trước khi thêm vào một khối mới trong blockchain. Và để làm được điều đó, hệ thống sẽ yêu cầu các nút mạng (nodes) phải giải quyết một bài toán toán học phức tạp được tạo ra bởi hàm POW.
-   Nút mạng tham gia vào tính toán được gọi là thợ đào (miners), và quá trình giải toán gọi là đào (mining). Cần có cộng đồng thợ đào để thực hiện một lượng công việc khổng lồ để giải mỗi phép toán nối tiếp nhau.
-   Để khai thác một khối mới trên blockchain, các thợ đào phải sử dụng sức mạnh tính toán của máy tính giải quyết một bài toán toán học phức tạp như tìm số nguyên dương nonce sao cho hàm băm (hash function) của nonce và dữ liệu khối (block data) là hash code có giá trị nhỏ hơn một ngưỡng cố định (difficulty target).
-   Khi một node giải quyết được bài toán POW, nó sẽ thông báo cho các nút khác trên mạng và các nút khác sẽ xác minh kết quả đó. Nếu kết quả đúng, khối mới sẽ được thêm vào blockchain, và node đã giải quyết bài toán POW sẽ được thưởng bằng một số tiền định trước của đồng tiền kỹ thuật số (như Bitcoin) hoặc các token khác. Sau khi khối mới được thêm vào blockchain, các giao dịch trong khối đó sẽ được xác nhận và được thêm vào danh sách các giao dịch hợp lệ trên blockchain. Các node khác trên mạng sẽ cập nhật lại blockchain của mình để phản ánh sự thay đổi này.

### `Ưu điểm`

-   Tính an toàn cao: POW là một cơ chế đồng thuận rất an toàn và được sử dụng trong nhiều blockchain lớn như Bitcoin và Ethereum. Cơ chế này đảm bảo rằng các giao dịch được xác nhận trên blockchain là chính xác và không bị thay đổi.
-   Tính bảo mật cao: PoW là cách tốt nhất để duy trì sự bảo mật và đồng thuận trong mạng phi tập trung. Lý do là PoW đòi hỏi phí tài nguyên và phần cứng liên tục, thay vì một khoản phí để tham gia như PoS. Giá trị Bitcoin ngày càng tăng lên đã khuyến khích nhiều nhà khai thác tham gia vào mạng lưới, đồng thời tăng sức mạnh và tính bảo mật của nó.
-   Tính khó tính toán: Thuật toán POW yêu cầu các nút trên mạng phải giải quyết một bài toán toán học phức tạp để tạo ra một khối mới trên blockchain. Quá trình giải quyết bài toán này yêu cầu nhiều sức mạnh tính toán và điện năng, làm cho việc tấn công blockchain thông qua POW rất khó khăn.
-   Tính công bằng: POW là một cơ chế đồng thuận công bằng, nghĩa là tất cả các nút trên mạng đều có cơ hội giải quyết bài toán POW và nhận được phần thưởng tương ứng. Điều này đảm bảo rằng không ai có thể kiểm soát quá trình xác nhận giao dịch và tạo ra khối mới trên blockchain.
-   Tính đồng nhất: POW đảm bảo tính đồng nhất của blockchain bằng cách yêu cầu tất cả các nút trên mạng phải đồng thuận về quá trình tạo ra khối mới trên blockchain. Nếu một nút trên mạng có ý định thay đổi lịch sử giao dịch của blockchain, nó sẽ phải giải quyết lại tất cả các bài toán POW từ đầu, điều này rất khó khăn và không thể thực hiện được.

### `Nhược điểm`

-   Tốn kém: Việc tạo ra một khối mới trên blockchain thông qua POW yêu cầu sử dụng rất nhiều sức mạnh tính toán và điện năng, điều này làm tăng chi phí hoạt động và gây ra ảnh hưởng đến môi trường.
-   Tốn thời gian: Người khai thác phải kiểm tra nhiều giá trị nonce để tìm ra giải pháp phù hợp cho câu đố phải giải để khai thác khối, đây là một quá trình tốn thời gian, do đó quá trình xác nhận giao dịch cũng chậm hơn so với các cơ chế đồng thuận khác.
-   Giảm tính phi tập trung: Bởi vì phần thưởng chỉ dành cho các thợ đào đầu tiên và các thợ đào khác không có thu nhập nên các thợ đào có xu hướng kết hợp lại với nhau, tạo nên các mining pool để có thể có một sức mạnh đủ lớn để tới đích trước. Việc này sẽ tạo ra một hệ quả khi một mining pool quá lớn trên 50% tổng số máy đào thì việc xác minh giao dịch sẽ không còn phi tập trung nữa và có thể bị thao túng bởi chính mining pool đó gây ra tính không minh bạch cho mạng lưới.
-   Rủi ro 51% : Nếu một thực thể kiểm soát sở hữu 51% hoặc hơn 51% số nút trong mạng, thì thực thể đó có thể làm hỏng chuỗi khối bằng cách giành được phần lớn mạng.

> ## POS (Proof of Stake)

###### Proof of Stake

</div>

### `Khái niệm`

-   Proof of Stake (POS) là một cơ chế đồng thuận thay thế cho Proof of Work trong blockchain dùng để xác thực và xác nhận giao dịch. Thay vì sử dụng sức mạnh tính toán để giải quyết các bài toán phức tạp để khai thác khối mới như POW, POS yêu cầu các node trong mạng đặt cược một số tiền tiền tệ kỹ thuật số nhất định của mình để đảm bảo tính đáng tin cậy của họ khi tham gia vào quá trình đồng thuận.
-   Thuật toán lựa chọn này kết hợp số lượng cổ phần (số tiền điện tử) với các yếu tố khác như lựa chọn dựa trên tuổi của đồng xu, quy trình ngẫu nhiên để làm cho lựa chọn công bằng cho mọi người trên mạng.
    -   Lựa chọn dựa trên tuổi tiền xu: Thuật toán theo dõi thời gian mỗi nút ứng cử viên trình xác thực vẫn là trình xác thực. Nút càng cũ thì cơ hội trở thành trình xác nhận mới càng cao.
    -   Lựa chọn khối ngẫu nhiên: Trình xác nhận được chọn với sự kết hợp của 'giá trị băm thấp nhất' và 'cổ phần cao nhất'. Nút có sự kết hợp trọng số tốt nhất trong số này sẽ trở thành trình xác thực mới.

### `Cơ chế hoạt động`

-   Khi một giao dịch mới được thêm vào mạng, các staker trong hệ thống POS sẽ cạnh tranh với nhau để trở thành validator (người xác thực) của khối đó.
-   Các staker cạnh tranh nhau bằng cách đặt cược (stake) một số tiền cố định vào hệ thống (ký gửi coin vào staking pool) để tham gia vào quá trình đánh giá độ tin cậy và cạnh tranh trở thành validator. Nếu một staker vi phạm các quy tắc của hệ thống POS, ví dụ như thực hiện gian lận trong quá trình đánh giá, thì họ sẽ bị phạt bằng việc mất một phần hoặc toàn bộ số tiền đang ký gửi trong hệ thống.
-   Hệ thống sẽ thực hiện việc chọn ngẫu nhiên một số staker để trở thành validator của khối đó, dựa trên mức độ đóng góp (như tuổi tiền xu) và số lượng tiền được đặt cược vào hệ thống của từng staker. Các staker có số tiền đặt cược lớn hơn sẽ có cơ hội cao hơn để được chọn trở thành validator.
-   Sau khi một staker được chọn làm validator cho khối mới, họ sẽ xác nhận giao dịch trong khối đó và tạo một chữ ký số cho khối mới. Sau đó, khối mới sẽ được broadcast (phát sóng) tới toàn bộ mạng và các staker khác sẽ xác thực chữ ký số của khối đó để đảm bảo tính toàn vẹn của khối và đồng thuận rằng khối mới được tạo ra chính xác. Sau khi khối mới được xác thực bởi đủ số lượng staker, nó sẽ được thêm vào chuỗi khối và trở thành phần của blockchain.
-   Sau khi validator đã xác thực khối mới và đóng góp vào mạng, họ sẽ nhận được phần thưởng cho việc tham gia vào quá trình đóng góp và giúp duy trì tính toàn vẹn của blockchain. Phần thưởng này thường được trả bằng đồng tiền của hệ thống blockchain đó. Ví dụ, trong Ethereum, validator sẽ nhận được đồng ETH làm phần thưởng.

### `Ưu điểm`

-   Tiết kiệm năng lượng: POS tiêu thụ ít năng lượng hơn so với POW vì không cần tính toán phức tạp và tiêu thụ điện năng lớn như trong POW.
-   Công bằng hơn: Với POS, tất cả các staker có cơ hội cạnh tranh trở thành validator, không chỉ những người có thể đầu tư vào phần cứng và điện năng đắt đỏ như trong POW.
-   Giảm nguy cơ tấn công 51%: Để tiến hành cuộc tấn công 51%, kẻ tấn công sẽ phải sở hữu 51% tổng số tiền điện tử trong mạng, điều này khá tốn kém. Điều này được coi là thực hiện cuộc tấn công quá tẻ nhạt, tốn kém và không mang lại nhiều lợi nhuận.
-   Khả năng mở rộng: POS cho phép các hệ thống blockchain mở rộng tốt hơn bằng cách tăng số lượng validator, mà không gặp những vấn đề về năng lượng và hiệu suất tính toán như trong POW.
-   An toàn và bảo mật: Một người cố gắng tấn công mạng sẽ phải sở hữu 51% cổ phần (rất tốn kém). Các staker trong hệ thống POS không cần phải trang bị phần cứng đắt tiền và thường không cần cài đặt phần mềm độc hại vào hệ thống, do đó giảm rủi ro bị hack và mất coin.

### `Nhược điểm`

-   Trình xác thực cổ phần lớn: Nếu một nhóm ứng cử viên trình xác thực kết hợp và sở hữu một phần đáng kể trong tổng số tiền điện tử, họ sẽ có nhiều cơ hội trở thành trình xác nhận hơn. Cơ hội tăng lên dẫn đến các lựa chọn tăng lên, dẫn đến việc kiếm được phần thưởng giả mạo ngày càng nhiều, dẫn đến việc sở hữu một phần tiền tệ khổng lồ. Điều này có thể khiến mạng trở nên tập trung theo thời gian (giảm tính phi tập trung của mạng).
-   Quy mô chưa lớn: Hệ thống PoS vẫn chưa mở rộng quy mô đến mức như Bitcoin hoặc Ethereum. Vì thế, chưa phi tập trung hoặc an toàn bằng các hệ thống PoW hàng đầu. Song, PoS có thể bắt kịp PoW nhờ khả năng mở rộng, rào cản gia nhập thấp hơn và không cần phần cứng chuyên dụng.
-   Nguy cơ chia tách mạng: POS có thể dẫn đến nguy cơ chia tách mạng nếu có nhiều phiên bản blockchain tồn tại. Nếu các validator không đồng ý với nhau, họ có thể tạo ra các phiên bản khác nhau của blockchain, dẫn đến sự không đồng bộ và mất tính toàn vẹn của mạng.

<br>

> ## DPoS (Delegated Proof of Stake)

###### Delegated Proof of Stake

</div>

### `Khái niệm`

-   Delegated Proof of Stake (DPoS) là một thuật toán đồng thuận được sử dụng trong blockchain để giải quyết vấn đề độ tin cậy và hiệu suất mà các thuật toán truyền thống khác không đáp ứng được.
-   Thuật toán DPoS phát triển từ Proof of Stake (POS), nhưng khác với POS, nó yêu cầu người dùng sở hữu token của blockchain để bỏ phiếu cho một số người đại diện được ủy quyền để đóng góp vào việc xác minh giao dịch và tạo khối. Những người được ủy quyền này được gọi là "witnesses" hoặc "delegates".

### `Cơ chế hoạt động`

-   Khi một giao dịch được gửi đến mạng blockchain, nó sẽ được truyền đến các nút mạng trong hệ thống. Sau đó, các witnesses hoặc delegates được ủy quyền sẽ xác minh và chứng minh tính hợp lệ của giao dịch đó. Các witnesses hoặc delegates này được chọn bởi cộng đồng sử dụng blockchain thông qua việc bỏ phiếu hoặc bằng cách sử dụng một hệ thống đại diện bao gồm một số lượng nhỏ các đại diện đáng tin cậy.
-   Sau khi giao dịch được xác nhận là hợp lệ, các witnesses hoặc delegates sẽ đóng vai trò trong việc tạo ra khối mới cho blockchain. Để làm điều này, các witnesses hoặc delegates sẽ thực hiện một số tính toán phức tạp để tìm ra một khối mới phù hợp với yêu cầu của mạng.
-   Khi khối mới được tạo ra, các witnesses hoặc delegates sẽ chèn các giao dịch mới vào khối và xác nhận chúng. Sau đó, khối mới này sẽ được truyền đến tất cả các nút trong mạng để được xác nhận. Sau khi xác nhận hoàn tất, phần thưởng sẽ được chia sẻ với những người bỏ phiếu cho witnesses hoặc delegates.

-   Ưu điểm:
    -   Khả năng xử lí giao dịch nhanh hơn PoW và PoS do đạt được sự đồng thuận nhanh hơn => Có khả năng mở rộng hơn và có thể được sử dụng cho nhiều ứng dụng.
    -   Các nhân chứng sẽ mất quyền đặt nếu họ thực hiện các hành vi độc hại => Động lực để họ thực hiện vai trò của mình một cách trung thực.
    -   Không cần thiết bị chuyên dụng để trở thành người dùng, nhân chứng hoặc người xác thực khối. Một máy tính bình thường với sức mạnh tính toán tốt là đủ.
    -   Chúng tiết kiệm năng lượng, tiết kiệm chi phí và thân thiện với môi trường so với các thuật toán băm PoW.
-   Nhược điểm:
    -   Có một nhóm nhỏ các nhân chứng được bầu có thể làm cho DPoS dễ bị tập trung hóa
    -   Bởi vì ít nút / nhân chứng hơn (20-100) chịu trách nhiệm giữ cho mạng tồn tại, nên việc tổ chức một cuộc tấn công 51% sẽ dễ dàng hơn.
    -   Sức mạnh bỏ phiếu được xác định bởi số lượng mã thông báo mà các cá nhân có, có nghĩa là những người sở hữu nhiều mã thông báo hơn sẽ ảnh hưởng đến mạng nhiều hơn những người sở hữu rất ít. Do đó, người dùng DPoS có cổ phần nhỏ sẽ có ít động lực bỏ phiếu hơn vì họ có thể nghĩ rằng phiếu bầu của họ không quan trọng so với phiếu bầu của các bên liên quan lớn hơn. Do đó, sự tham gia thấp vào quá trình bỏ phiếu có thể tạo ra sự tập trung hơn nữa trong mạng bằng cách đặt quyền lực vào tay một số lượng hạn chế chủ sở hữu tiền xu.

---
