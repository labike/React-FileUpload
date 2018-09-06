# React-FileUpload
upgrade support React@16.X

project from https://github.com/SoAanyip/React-FileUpload

#### Use

if React@15.X to https://github.com/SoAanyip/React-FileUpload

if React16.X
new file `newFileUpload.js`
copy `FileUpload.js` code to `newFileUpload.js`

custom component content:

    import FileUpload from 'FileUpload'
    
    class NewFileUpload extends Component{
        render(){
            /*set properties*/
            const options={
                baseUrl:'/xxx/xxx/xxx.php',
                fileFieldName: 'upload_file',
                dataType: 'json',
                chooseAndUpload: true,
                uploadSuccess: (res) => this.props.onSuccess(res.data),
                uploadError: (err) => this.props.onError(err.message || '上传图片出错')
            }
            /*Use FileUpload with options*/
            /*Set two dom with ref*/
            return (
                <FileUpload options={options}>
                    <button className="btn btn-xs btn-default" ref="chooseAndUpload">请选择图片</button>
                </FileUpload>
            )
        }	        
    }
    
    export default NewFileUpload
  

